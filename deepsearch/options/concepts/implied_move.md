---
title: Implied Move（隐含波动幅度 / Expected Move）
date: 2026-08-09
tags: [concept, options, volatility]
status: final
---

从期权价格反推出的市场对事件波动的定价。财报场景近似算法：近月 ATM 跨式价格 ÷ 股价 ≈ 市场预期的财报后涨跌幅。例：隐含 ±7.2% 意味着市场定价财报后股价有 ~68% 概率落在 ±7.2% 内。

**对本策略的意义**：决策的锚点。研究的核心问题就是「我们认为实际波动会大于还是小于 implied move」。判断大于 → 买方策略；小于 → 卖方策略吃 [[IV_crush]]。

关联：[[volatility_risk_premium]]、[[IV_crush]]、[[PEAD]]
