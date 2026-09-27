---
type: finding
title: 行列式与反称 n 线性型的关系
source: "[[10-数学指南实用数学手册--11-242-多线性型的计算--1934obg]]"
confidence: high
replicated: null
tags: [多线性代数, 行列式, 反称性]
related: [多线性型, 行列式, 反称多线性型, 线性算子, 10-数学指南实用数学手册--11-242-多线性型的计算--1934obg]
sources: ["数学指南_实用数学手册/2.4.2 多线性型的计算.md"]
created: 2026-09-27
updated: 2026-09-27
---

# 行列式与反称 n 线性型的关系

设 $A: X \to X$ 是 $\mathbb{K}$ 上 $n$ 维线性空间上的线性算子。《数学指南》2.4.2 节给出

$$
M(Au_{1}, \dots , Au_{n}) = (\det A)\, M(u_{1}, \dots , u_{n})
$$

对于所有反称 $n$ 线性型 $M: X \times \cdots \times X \rightarrow K$ 及所有 $u_{1}, \cdots, u_{n} \in X$。

也就是说：反称 $n$ 线性型是 $\det A$ 的一个"特征向量方向"——算子 $A$ 作用在全部自变量上等价于整体乘以 $\det A$。这与 [[行列式]] 的乘法性质（$\det(AB) = \det A \det B$）相容，也是 [[外积与行列式理论相关]] 的直接来源。

## 关联

- [[多线性型]]
- [[findings/外积与行列式理论相关]]
- [[findings/例2三重外积等于行列式]]
