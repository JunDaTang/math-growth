---
type: finding
title: 正态密度在均值处取极大值且 sigma 越小越集中
created: 2026-09-27
updated: 2026-09-27
tags: [数理统计, 正态分布, 概率密度]
related: [正态分布, 高斯钟形曲线, 概率密度]
sources: ["数学指南_实用数学手册/0.4.2 理论分布函数.md"]
source: "[[10-数学指南实用数学手册--10-042-理论分布函数--118ygtx]]"
confidence: high
replicated: null
---

# 正态密度在均值处取极大值且 sigma 越小越集中

源对 (0.48) 给出的高斯钟形曲线

$$
\varphi(x) := \frac{1}{\sigma\sqrt{2\pi}}\mathrm{e}^{-(x-\mu)^2/2\sigma^2}
$$

陈述两点形态事实：

1. 曲线在 $x = \mu$ 处有极大值；
2. 正数 $\sigma$ 越小，曲线就越向点 $x = \mu$ 处集中。

## 证据类型

这是源中的直接陈述，属理论性（数学）事实而非经验测量结果，因此不存在「复现」意义上的重复实验；`replicated` 记为 null。密度最大值可由对指数项取最大得到，属可直接验证的推论。