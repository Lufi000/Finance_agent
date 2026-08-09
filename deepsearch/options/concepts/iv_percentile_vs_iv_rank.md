---
title: IV Percentile vs IV Rank
date: 2026-08-09
tags: [concept, options, volatility]
status: final
---

- **IV Rank (IVR)**：当前 IV 在过去一年 IV 最高/最低区间中的位置。缺点：被少数尖峰（如一年 4 次财报）拉高上限后，平时段 IVR 被压缩失真
- **IV Percentile (IVP)**：过去一年中 IV 低于当前值的天数占比。对尖峰不敏感

**对本策略的意义**：财报策略**以 IVP 为准（入选阈值 ≥ 80），IVR 仅辅助**。这是 [[earnings_iv_landscape]] 调研后回写 [[PLAYBOOK]] 的修正之一。

关联：[[IV_crush]]、[[volatility_risk_premium]]
