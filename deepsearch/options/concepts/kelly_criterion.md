---
title: Kelly Criterion（凯利公式）与仓位纪律
date: 2026-08-09
tags: [concept, risk, sizing]
status: final
---

f* = p − q/b（p 胜率，q=1−p，b 盈亏比）。理论上最大化长期复利的仓位比例，但实战中全额 Kelly 波动过大，业界常用 **10% Kelly**（开源项目 earnings-trade-automation 即采用）。

**对本策略的意义**：[[PLAYBOOK]] 的仓位规则 = 单笔风险敞口 ≤ 账户 2%（对齐机构 vol desk 实践），决策简报里 Agent 给出 Kelly 校准参考值，用户拍板。胜率/盈亏比的历史估计来自 [[2026]] 交易日志与复盘的滚动样本——**这就是复盘必须回写的原因**。

关联：[[PLAYBOOK]]
