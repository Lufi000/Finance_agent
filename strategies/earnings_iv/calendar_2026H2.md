---
title: 美股财报日历 2026H2（8月–12月）× 财报IV策略初判
date: 2026-08-09
tags: [strategy, earnings, calendar, options]
status: draft
---

> 报告日期：2026-08-09
> 数据来源：Earnings Today 财经日历（8–12 月页面，2026-08-09 抓取）[^1^]、公司 IR 公告与多来源交叉验证[^2^][^3^]
> **仅供研究参考，不构成投资建议；所有交易由用户手动执行。**

按 [[PLAYBOOK]] 筛选标准对到年底的财报事件做**第一层初判**。注意：[[iv_percentile_vs_iv_rank|IV percentile ≥ 80]] 只能在 T-14 窗口用实时数据判定，本日历的初判基于**市值/期权流动性/历史财报后实际波动**三个可先验的维度。

## 初判图例

| 标记 | 含义 | 判定依据 |
|---|---|---|
| ✅ | 重点候选 | 历史财报后波动大（典型 \|move\| ≥ 6%）、期权链流动性好、事件定价博弈充分，[[IV_crush]] 卖方与 [[implied_move]] 买方两个方向都值得研究 |
| 🟡 | 观察 | 可做但性价比一般：波动温和（卖方薄利）或流动性/中小盘折价（买方成本高），须等 T-14 数据再定 |
| ❌ | 排除 | 财报波动常年过低（IV 也低，双方向都没肉）、定价失真（meme 属性）或期权链不达标；按 PLAYBOOK「拿不准 = 放弃」 |

日期标注：**确认** = 公司已公告或多来源一致；**预估** = 日历站推算；**预估\*** = 本站暂无数据，按上一财季同日历年同周推算，T-14 必须复核官方 IR。

---

## 8 月（8/10 起，Q2 财报季收尾）

| 日期 | 标的 | 时间 | 日期状态 | 初判 | 原因 |
|---|---|---|---|---|---|
| 08-10 | RKLB | AMC | 确认 | 🟡 | 中小盘高波动，但期权链薄、买卖价差宽，若做按中小盘纪律减半仓位 |
| 08-12 | CSCO | AMC | 确认 | 🟡 | 历史 move ~4–5%，波动温和，[[volatility_risk_premium]] 卖方候选；AI 网络叙事有上行尾部，卖方须用有限风险结构 |
| 08-13 | AMAT | AMC | 确认 | ✅ | 半导体设备，move ~6–8%，WFE 周期 + 中国敞口双向博弈充分 |
| 08-13 | NU | — | 预估 | 🟡 | ADR 流动性一般，价差偏宽 |
| 08-18 | HD | BMO | 确认 | 🟡 | move ~3–4%，卖方薄利；地产链数据有宏观外溢价值 |
| 08-19 | ADI | BMO | 确认 | 🟡 | 模拟芯片，move ~5%，工业/汽车周期拐点博弈 |
| 08-19 | TGT | BMO | 确认 | 🟡 | **修正（8/11 实测）**：近 8 次实际波动均值仅 1.6%、最大 3.1%，隐含 8.2% —— 隐含/实际 5.2x，**卖方候选**而非高波买方标的 |
| 08-19 | LOW | BMO | 确认 | 🟡 | 跟随 HD，move ~4% |
| 08-19 | TJX | BMO | 确认 | ❌ | 折扣零售低波动（~2–3%），双方向无肉 |
| 08-20 | WMT | BMO | 确认 | 🟡 | 防御属性，move ~3–4%，仅适合卖方且薄利 |
| 08-20 | ROST | — | 预估 | 🟡 | 同 TJX 但波动略高 |
| 08-21 | BJ | BMO | 确认 | 🟡 | 中盘零售，期权链一般 |
| 08-25 | INTU | AMC | 确认 | 🟡 | move ~5–6%，税务软件季节性弱 |
| 08-25 | ZM | AMC | 确认 | ❌ | 波动结构性衰减，期权链流动性持续恶化 |
| **08-26** | **NVDA** | AMC | **确认**[^2^] | ✅ | **全市场最重事件**，move ~6–9%；近两年 IV 系统性高估实际波动，[[IV_crush]] 卖方与超预期买方均需深度研究，T-14 启动 |
| 08-26 | CRM | AMC | 确认 | ✅ | move ~6–8%，Agentforce 货币化分歧大 |
| 08-26 | CRWD | AMC | 确认 | ✅ | move ~10%+，但估值高、尾部厚，卖方必须铁鹰/价差 |
| 08-27 | MRVL | AMC | 确认 | 🟡 | **修正（8/11 实测）**：实际波动均值 10.9%、双尾 ±20% 级别，隐含 18.1% 仅 1.7x——拿不准=放弃 |
| ~~08-27~~ | DELL | AMC | 确认 | ✅ | **修正（8/11 核实）：财报日为 09-03**。近两次实际 +22%/+33% 超过隐含——**买方候选**（call 价差），T-14 复核 |

## 9 月（Q2 补报 + 财政年度错位股）

| 日期 | 标的 | 时间 | 日期状态 | 初判 | 原因 |
|---|---|---|---|---|---|
| 09-01 | PANW | AMC | 确认 | ✅ | move ~8–10%，网安平台化叙事 |
| 09-01 | MDB | AMC | 确认 | ✅ | move ~15% 级别，高波动代表，但注意流动性折价 |
| 09-01 | MDT | BMO | 确认 | ❌ | 医疗器械低波（~2–3%） |
| 09-02 | SNOW | AMC | 确认 | ✅ | move ~10–15%，增速 vs 估值永久博弈 |
| 09-02 | LULU | — | 预估 | ✅ | move ~10%+，美洲增长失速争议 |
| 09-02 | HPE | — | 预估 | 🟡 | move ~5–6%，Juniper 并表整合期 |
| 09-02 | DLTR | — | 预估 | 🟡 | 低价零售，波动中等 |
| **09-03** | **AVGO** | — | 预估 | ✅ | **AI ASIC 核心标的**，move ~8–10%；上一财年同日 9/4 财报 |
| 09-08 | ORCL | — | 预估 | ✅ | 云基建 RPO 叙事使波动结构性放大（2025-09 财报曾单日 +36%），卖方慎用 |
| 09-08 | GME | — | 预估 | ❌ | meme 定价失真，波动无基本面锚，尾部不可控 |
| 09-10 | ADBE | — | 预估 | ✅ | AI 颠覆叙事下多次 ±10%，分歧极大 |
| 09-10 | RH | — | 预估 | 🟡 | 中盘高波但期权链薄 |
| 09-22 | MU | — | 预估 | ✅ | HBM 周期核心，move ~8–10% |
| 09-22 | AZO | — | 预估 | ❌ | 汽车零件零售低波 |
| 09-24 | COST | — | 预估 | 🟡 | move ~2–3%，仅卖方薄利 |
| 09-28 | CCL | — | 预估 | 🟡 | 邮轮周期股，move ~5–6% |
| 09-29 | NKE | — | 预估 | 🟡 | 转型期波动回升至 ~6%，观察 |

## 10 月（Q3 财报季主战场）

| 日期 | 标的 | 时间 | 日期状态 | 初判 | 原因 |
|---|---|---|---|---|---|
| 10-08 | PEP | — | 预估 | ❌ | 必需消费低波 |
| 10-12 | FDX | — | 预估 | 🟡 | 物流宏观晴雨表，move ~5% |
| 10-13 | JPM | BMO | 预估* | 🟡 | 财报季风向标，但银行 move ~2–3%，卖方薄利；主要价值是宏观情报 |
| 10-13 | C / GS | — | 预估 | 🟡 | 同上 |
| 10-14 | ASML | — | 预估 | ✅ | move ~6–8%，EUV 订单 + 中国出口管制双向催化 |
| 10-14 | BAC / MS / BLK | — | 预估 | 🟡 | 银行/资管低波 |
| 10-14 | ABT | — | 预估 | ❌ | 低波医疗 |
| 10-15 | TSM | — | 预估 | ✅ | ADR，AI 资本开支风向标，move ~4–5%，指引影响整个半导体链 |
| 10-15 | SCHW / PNC / USB | — | 预估 | ❌ | 区域银行低波 |
| 10-20 | **NFLX** | AMC | 预估[^3^] | ✅ | **move ~8–12%**，广告层 + 内容支出博弈，历史 IV 常低估尾部 |
| 10-20 | KO / VZ | — | 预估 | ❌ | 低波防御 |
| 10-20 | GE / RTX / IBKR | — | 预估 | 🟡 | 中等波动 |
| **10-21** | **TSLA** | AMC | 预估[^3^] | ✅ | **move ~8–12%**，机器人/ Robotaxi 叙事 vs 汽车基本面，IV 极高但尾部真实存在，方向逐案 |
| 10-21 | IBM / TMO / PM | — | 预估 | 🟡 | 中等偏低波动 |
| 10-22 | INTC | — | 预估 | ✅ | 代工转型赌注，move ~8–12%，事件驱动特征强 |
| 10-22 | TMUS / NEM / FCX | — | 预估 | 🟡 | 电信/矿业中等波动 |
| 10-23 | AXP / SLB | — | 预估 | 🟡 | 中等波动 |
| 10-27 | **MSFT** | AMC | 预估* | ✅ | Azure 增速 + AI capex 核心事件，move ~4–6%；波动温和使**卖方 [[IV_crush]] 候选**价值更高 |
| 10-27 | TXN | — | 预估 | 🟡 | move ~4–5%，工业半导体晴雨表 |
| 10-27 | UNH | — | 预估 | 🟡 | 2025 年起波动放大至 ~7%，但属政策事件驱动，难以定价 |
| 10-28 | **META** | AMC | 预估* | ✅ | AI capex vs 广告变现，move ~7–10% |
| 10-28 | **GOOGL** | AMC | 预估 | ✅ | 搜索反垄断 + Gemini 竞争，move ~5–7% |
| 10-28 | NOW | — | 预估 | ✅ | 企业软件高 beta，move ~7–9% |
| 10-28 | BA / GEV | — | 预估 | 🟡 | BA 事件风险非财报化；GEV 电力设备热度高但连锁已炒作 |
| **10-29** | **AMZN** | AMC | 预估* | ✅ | AWS 增速 + 零售利润率，move ~6–8% |
| 10-29 | **AAPL** | AMC | 预估* | 🟡 | move 仅 ~3–4%，但期权链全球最深，**卖方吃 crush 的优质薄利标的** |
| 10-29 | V / MA | — | 预估* | 🟡 | 低波（~2–3%），消费数据情报价值 |
| 10-29 | CMCSA / CHTR | — | 预估 | ❌ | 有线电视低波 |

## 11 月（Q3 收尾：半导体二轮 + 零售）

> 本站暂无 11 月录入，以下全部为**预估\***（按 2025 年同财季同周推算），T-14 必须复核。

| 日期 | 标的 | 初判 | 原因 |
|---|---|---|---|
| 11-02 | PLTR | ✅ | move ~10–15%，政府/商用 AI 订单博弈，散户情绪放大器 |
| 11-03 | AMD | ✅ | MI 系列 vs NVDA 竞争格局，move ~8–10% |
| 11-03 | SMCI | ✅ | 高波动但治理有前科，仓位从严 |
| 11-04 | QCOM | 🟡 | move ~5–6%，手机周期 + 自研 PC 芯片 |
| 11-04 | ARM | ✅ | 估值极贵 + 授权模式分歧，move ~10% |
| 11-04 | HOOD | ✅ | 散户交易活跃度直接挂钩，move ~10% |
| 11-17 | HD | 🟡 | 同 8 月逻辑 |
| 11-18 | PANW | ✅ | 同 9 月逻辑 |
| 11-18 | LOW / TGT | 🟡 | 同 8 月逻辑 |
| **11-18** | **NVDA** | ✅ | **Q3 财报，全年最重要节点之一**（2025 年为 11-19） |
| 11-19 | WMT | 🟡 | 同 8 月逻辑 |
| 11-24 | DELL | ✅ | 同 8 月逻辑 |

## 12 月（财政年度错位股专场）

> 本站暂无 12 月录入，以下全部为**预估\***。

| 日期 | 标的 | 初判 | 原因 |
|---|---|---|---|
| 12-01 | CRWD | ✅ | 同 8 月逻辑 |
| 12-02 | SNOW / CRM | ✅ | 同前逻辑（CRM 上财年 Q3 为 2025-12-03[^4^]） |
| 12-03 | MRVL / LULU | ✅ | 同前逻辑 |
| 12-09 | ORCL | ✅ | 同 9 月逻辑（上财年 Q2 为 2025-12-10[^5^]） |
| 12-10 | AVGO | ✅ | Q4 财报 + 下年 AI 指引，年末半导体定调事件 |
| 12-10 | ADBE / COST | ✅ / 🟡 | ADBE 同前；COST 低波 |
| 12-16 | MU | ✅ | HBM 供需年度指引 |
| 12-17 | NKE | 🟡 | 转型进度检查 |

---

## 策略衔接

- **T-14 滚动维护**：每周日扫描本日历，把进入 T-14 窗口的标的迁入 [[watchlist]]，拉取实时 IV percentile / [[implied_move]] / 期限结构，完成第二层筛选
- **当前 T-14 窗口**（8/10–8/23）：RKLB、CSCO、AMAT、HD、ADI、TGT、LOW、WMT 等已迁入 watchlist
- **双月重点**：8/26 NVDA（确认）是全月锚点；10/20–10/29 是全年密度最高的超级周（NFLX→TSLA→MSFT→META/GOOGL→AMZN/AAPL），提前规划研究排期，避免 T-1 撞车
- 复盘结论回写 [[PLAYBOOK]] 筛选标准，初判准确率本身也纳入复盘（T+1 对照「初判 vs 实际是否有利可图」）

## 数据来源

[^1^]: Earnings Today 月度日历：[2026-08](https://www.earningstoday.com/earnings-calendar/monthly/2026-08)、[2026-09](https://www.earningstoday.com/earnings-calendar/monthly/2026-09)、[2026-10](https://www.earningstoday.com/earnings-calendar/monthly/2026-10)、[2026-11](https://www.earningstoday.com/earnings-calendar/monthly/2026-11)、[2026-12](https://www.earningstoday.com/earnings-calendar/monthly/2026-12)，抓取于 2026-08-09；其中 11/12 月录入尚不完整
[^2^]: [NVIDIA Sets Conference Call for Second-Quarter FY27 Financial Results](https://nvidianews.nvidia.com/news/nvidia-sets-conference-call-for-second-quarter-financial-results-6927195)（2026-08-26，AMC 5:00pm ET），另经 [Nasdaq](https://www.nasdaq.com/market-activity/stocks/nvda/earnings)、[Public.com](https://public.com/stocks/nvda/earnings) 交叉确认，访问于 2026-08-09
[^3^]: [Public.com NFLX Earnings](https://public.com/stocks/nflx/earnings)（10-20）、[Public.com TSLA Earnings](https://public.com/stocks/tsla/earnings) / [EarningsCountdown TSLA](https://earningscountdown.com/stock/tsla)（10-21），均为估计值、官方未确认，访问于 2026-08-09
[^4^]: [Salesforce FY26 Q3 Results](https://www.salesforce.com/news/press-releases/2025/12/03/fy26-q3-earnings/)，2025-12-03，用于推算 2026-12 节奏
[^5^]: [Oracle Q2 FY26 Earnings Date Announcement](https://investor.oracle.com/investor-news/news-details/2025/Oracle-Sets-the-Date-for-its-Second-Quarter-Fiscal-Year-2026-Earnings-Announcement/default.aspx)，2025-12-10，用于推算 2026-12 节奏

> 历史财报后波动幅度（move %）为基于过往 8 个季度公开行情的经验量级，用于初判分层；精确值在 T-14 深度研究时按当时数据重新计算。
