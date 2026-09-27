---
type: finding
title: 例：$-y'' = \lambda y$ 在 [0, π] 上的本征函数 sin nx 与本征值 n²
source: "[[10-数学指南实用数学手册--14-1128-边值问题和格林函数--1qd4d88]]"
confidence: high
replicated: false
created: 2026-09-27
updated: 2026-09-27
tags: [本征值问题, 例题, 正弦级数]
related: [本征值问题, 广义傅里叶级数, 本征值问题1313与存在性定理四条]
sources: ["数学指南_实用数学手册/1.12.8 边值问题和格林函数.md"]
---

# 例：$-y'' = \lambda y$ 在 [0, π] 上的本征函数 sin nx 与本征值 n²

**来源**：《数学指南——实用数学手册》1.12.8.3 节（[[10-数学指南实用数学手册--14-1128-边值问题和格林函数--1qd4d88]]）。

## 直接陈述（源中明确给出）

$$
- y'' = \lambda y, \quad 0 \leqslant x \leqslant \pi, \quad y(0) = y(\pi) = 0
$$

有本征函数

$$
y_n = \sin n x
$$

和本征值

$$
\lambda_n = n^2, \quad n = 1, 2, \cdots .
$$

## 备注

这是 (1.313) 在 $p \equiv 1$、$q \equiv 0$、$[a,b] = [0,\pi]$ 下的特例。本征函数在 $(0,\pi)$ 内部恰有 $n-1$ 个零点（$\sin nx$ 的零点 $k\pi/n$，$k = 1, \dots, n-1$），与存在性定理 (iii) 一致；本征值互不相同（单重），与 (ii) 一致；$\lambda_n = n^2 \to +\infty$，与 (i) 一致；$\lambda_1 = 1 > \min q = 0$，与 (iv) 一致。

相关：[[findings/本征值问题1313与存在性定理四条]]、[[concepts/广义傅里叶级数]]。
