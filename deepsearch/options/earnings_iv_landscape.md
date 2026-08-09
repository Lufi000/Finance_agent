---
title: 财报IV策略行业调研：开源项目、学术研究与量化实践
date: 2026-08-09
tags: [strategy, options, earnings, IV, deepsearch]
status: final
---

> 调研日期 2026-08-09。目的：对照 [[PLAYBOOK]]，看开源社区、学术界、量化机构在「财报 + 高 IV」策略上的成熟做法。仅供研究参考，不构成投资建议。

## 一、核心结论（TL;DR）

1. **学术界确认财报事件的隐含波动系统性高估实际波动**（implied > realized，见 [[volatility_risk_premium]]），卖方有结构性 edge[^1^]
2. **但卖方收益分布是负偏的**：QuantConnect 社区回测显示裸卖跨式/宽跨式的小额频繁盈利会被少数极端财报波动一次性抹掉，即使叠加 IV percentile 过滤[^2^]→ **成熟玩家普遍用有限风险结构**（铁鹰、日历价差）而非裸卖
3. **IV Rank 对财报股会失真**（见 [[iv_percentile_vs_iv_rank]]），财报策略应优先看 **IV percentile**，阈值要比常规卖方策略高得多（IVR > 70、IVP > 80）[^3^]
4. **tastytrade 研究**：高 IVR 提升的是单笔盈亏而非胜率（SPY 宽跨胜率各 IVR 桶均在 77–84%，但平均 P/L 从 $34 翻倍到 $72）[^4^]；独立回测（SJ Options）则质疑 IVR>50 卖价差在扣费后并无优势[^5^]→ 高 IV 是必要条件而非充分条件
5. **机构做法**：财报季是个股特异性波动（idiosyncratic vol）的主要来源，vol desk 围绕它做 [[dispersion_trading]] / 事件驱动交易，仓位很小（0.5–2%，仓位方法见 [[kelly_criterion]]），并买远端便宜翅膀做尾部保护[^6^]

## 二、值得关注的开源项目

| 项目 | 星标 | 可借鉴点 |
|---|---|---|
| [ProgramComputer/earnings-trade-automation](https://github.com/ProgramComputer/earnings-trade-automation) | 中 | **最对口**：财报日历价差自动化 bot。筛选=期限结构倒挂 + IV/RV 比率 + 成交量；**10% Kelly 仓位公式**；用 ATM 日历价差替代裸卖跨式降低尾部风险[^7^] |
| [kenchengkc/quantiv](https://github.com/kenchengkc/quantiv) | 6★ | 从实时期权链计算财报 expected move 的看板，含历史对比 |
| [Digantdc/iv-mean-reversion](https://github.com/Digantdc/iv-mean-reversion) | 0★ | IV 均值回归画像：AR(1) 粘性、半衰期、**财报 crush 统计、VRP 度量**，IBKR 数据源 |
| [expandingourselves/IV_Trade_App](https://github.com/expandingourselves/IV_Trade_App) | 0★ | 单标的打分卡：ATM IV 期限结构 + expected move + 流动性检查 → Recommended/Consider/Avoid，和我们的决策简报思路一致 |
| [mauidoza/Options-EDGE](https://github.com/mauidoza/Options-EDGE) | 0★ | A–D 评级扫描器，覆盖 IVP、流动性等 7 因子 |
| [RupertDodkins/options_backtest](https://github.com/RupertDodkins/options_backtest) | — | 基于 QuantConnect/Lean 的多腿策略回测框架 |
| [AlexCrescentini/backtest_spx_vanilla_options](https://github.com/AlexCrescentini/backtest_spx_vanilla_options) | — | 多腿策略回测，含前向分析排除起始日运气 |

**观察**：这个细分领域的开源项目普遍星标很低，没有"明星项目"——说明成熟玩家要么用商业数据平台（ORATS、OptionMetrics、ivolatility），要么策略闭源。我们的 Agent + 人工决策模式反而是差异化。

## 三、学术与量化研究要点

- **Todorov (Northwestern Kellogg)**：用短周期期权检验事件时刻的跳跃强度变化，发现期权隐含的财报跳跃波动平均高于实际实现值——财报 IV 溢价的学术实锤[^1^]
- **Princeton 2024 毕业论文（Eric Ahn）**：从期权提取"priced-in 财报波动"，用历史财报波动、**分析师预测分歧度**、公司规模建立预测模型——分析师分歧度是可加入我们筛选层的信号[^8^]
- **ORATS 的 NVDA 案例**：直接对比本次 [[implied_move|隐含波动]] 7.2% vs 过去 12 个季度实际波动均值 7.3%[^9^]——和我们 PLAYBOOK 的「隐含 vs 历史实际」对比完全一致，说明方法论对路
- **[[PEAD]]（财报后漂移）**：财报跳空后倾向沿原方向漂移，买方策略持有期内可利用[^6^]
- **分析师分歧度组合策略**（Quantpedia 收录）：按 I/B/E/S 预期分歧度分组，对高分歧股票买 put + 卖指数 put，历史年化 ~15%[^6^]

## 四、机构 vol desk 的实操细节

1. **T-3 周到 T-1 周**：交易 "IV ramp"（事件不确定性被重新定价的过程）
2. **事件时**：卖最近周期权跨式吃跳跃溢价 + IV crush；**仓位 0.5–2%**，买远端便宜翅膀防尾部
3. **事件后**：IV 回落、实际波动兑现后平仓（vol-arb harvesting）
4. 最大风险是**相关性冲击**（宏观事件让个股同向暴跌），个案层面体现为财报暴雷叠加大盘风险[^6^]

## 五、对我们 PLAYBOOK 的修正（已回写）

> 概念索引见 [[options_MOC]]；每个概念有独立原子笔记（`concepts/`），后续所有标的研究会自动挂接到图谱。

| 原条款 | 修正 | 依据 |
|---|---|---|
| IV Rank ≥ 50 | 财报策略改看 **IV percentile ≥ 80**（IVR 仅作辅助，因财报尖峰失真） | [^3^] |
| 未限制结构 | 卖方默认**有限风险结构**（铁鹰/价差），裸卖需用户明示同意 | [^2^][^6^] |
| 无统一仓位规则 | 单笔风险敞口默认 ≤ 账户 2%，参考 10% Kelly | [^6^][^7^] |
| 筛选无量化比率 | 增加 **IV/RV 比率** 与**期限结构倒挂**作为入选加分项 | [^7^] |
| 研究层无分歧度 | 研究简报增加**分析师预测分歧度**字段 | [^8^] |

## 来源

[^1^]: [Testing for Anticipated Changes in Spot Volatility at Event Times — Todorov, Kellogg](https://www.kellogg.northwestern.edu/faculty/todorov/htm/papers/vet.pdf)（访问 2026-08-09）
[^2^]: [QuantConnect Forum: Earnings IV Crush](https://www.quantconnect.com/forum/discussion/19812/earnings-iv-crush/)（访问 2026-08-09）
[^3^]: [Volatility Box: IV Rank vs IV Percentile](https://volatilitybox.com/research/iv-rank-vs-iv-percentile/)（访问 2026-08-09）
[^4^]: [tastylive: The Impact of High IV on Trading Profits](https://www.tastylive.com/news-insights/The-Impact-of-High-Implied-Volatility-IV-on-Trading-Profits)（访问 2026-08-09）
[^5^]: [SJ Options: High IV Rank vs Low IV Rank Credit Spreads](https://www.sjoptions.com/high-iv-rank-vs-low-iv-rank-credit-spreads/)（访问 2026-08-09）
[^6^]: [Trading Riot: Volatility Trading Around Earnings](https://blog.tradingriot.com/p/volatility-trading-around-earnings)；[Hedgeweek: Hedge funds refine dispersion trades](https://www.hedgeweek.com/hedge-funds-refine-dispersion-trades-amid-market-volatility-shift/)（访问 2026-08-09）
[^7^]: [GitHub: ProgramComputer/earnings-trade-automation](https://github.com/ProgramComputer/earnings-trade-automation)（访问 2026-08-09）
[^8^]: [Princeton senior thesis: Eric Ahn 2024](https://drigobon.com/senior-thesis-advisees/2024_Eric_Ahn.pdf)（访问 2026-08-09）
[^9^]: [ORATS: NVIDIA Earnings Volatility Preview](https://orats.com/blog/nvidia-earnings-volatility-preview-orats-data)（访问 2026-08-09）
