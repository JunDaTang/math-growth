---
type: finding
title: 例 1：$-y'' = f$ 在 [0,1] 上的格林函数
source: "[[10-数学指南实用数学手册--14-1128-边值问题和格林函数--1qd4d88]]"
confidence: high
replicated: false
created: 2026-09-27
updated: 2026-09-27
tags: [格林函数, 例题, 边值问题]
related: [格林函数, 边值问题, 弗雷德霍姆择一性]
sources: ["数学指南_实用数学手册/1.12.8 边值问题和格林函数.md"]
---

# 例 1：$-y'' = f$ 在 [0,1] 上的格林函数

**来源**：《数学指南——实用数学手册》1.12.8.1 节（[[10-数学指南实用数学手册--14-1128-边值问题和格林函数--1qd4d88]]）。

## 直接陈述（源中明确给出）

对每个连续函数 $f:[0,1] \to \mathbb{R}$，边值问题

$$
- y'' = f(x), \quad \text{在} [0,1] \text{上}, \quad y(0) = y(1) = 0
$$

有唯一解

$$
y(x) = \int_{0}^{1} G(x, \xi) f(\xi) \mathrm{d} \xi ,
$$

其中

$$
G(x, \xi) := \left\{ \begin{array}{ll} x(1 - \xi), & 0 \leqslant x \leqslant \xi \leqslant 1, \\ \xi(1 - x), & 0 \leqslant \xi \leqslant x \leqslant 1. \end{array} \right.
$$

源中说明：解的唯一性从唯一性条件 (b) 即得（此处 $p \equiv 1$、$q \equiv 0$，故 $\max_{[0,1]} q = 0 \geqslant 0$）。

## 性质

该 $G$ 关于 $x, \xi$ 对称，且在两段上的表达式在 $x = \xi$ 处连续（取值 $x(1-x)$）。这是本节唯一给出的非平凡显式格林函数。

相关：[[concepts/格林函数]]、[[concepts/弗雷德霍姆择一性]]。
