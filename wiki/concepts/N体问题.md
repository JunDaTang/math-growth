---
type: concept
title: N 体问题
created: 2026-09-27
updated: 2026-09-27
tags: [经典力学, 牛顿定律, 多体系统, 轨道]
related: [牛顿基本运动定律, 轨道, 存在性与唯一性定理, 守恒律, 行星运动, 保守力]
sources: ["数学指南_实用数学手册/1.9.6 对力学的守恒律的应用.md"]
---

# N 体问题

$N$ 体问题是经典力学中 $N$ 个质点（数目任意）在彼此相互作用下的运动问题。其运动由《数学指南——实用数学手册》1.9.6 节给出的方程组 (1.163) 描述：

$$
m_{j} \boldsymbol{r}_{j}^{\prime \prime}(t) = \boldsymbol{F}_{j}(\boldsymbol{r}_{1}, \dots, \boldsymbol{r}_{N}, \boldsymbol{r}_{1}^{\prime}, \dots, \boldsymbol{r}_{N}^{\prime}, t), \quad j = 1, \dots, N,
$$

配合初始条件 (1.164)：

$$
\boldsymbol{r}_{j}(0) = \boldsymbol{r}_{j 0}, \quad \boldsymbol{r}_{j}^{\prime}(0) = \boldsymbol{r}_{j 1}, \quad j = 1, \dots, N.
$$

第 $j$ 个质点所受的力 $F_j$ 一般依赖于全部质点的位置、全部质点的速度以及时间 $t$。方程组的解是 $N$ 条轨道 $r_j = r_j(t)$。

为了简化记号，原文令 $r := (r_1, \cdots, r_N)$，即把 $N$ 个位置向量整体记作一个「超向量」$r$；力的分解式 $F_j = -\operatorname{grad}_{r_j} U(r) + F_{j*}$ 与势能 $U(r)$ 都建立在这一记号之上。

## 与单体形式的区别

- [[concepts/牛顿基本运动定律]]只讨论单个质点的 $F = ma$；N 体问题把它逐分量地并列成 $N$ 个方程，并通过力 $F_j$ 使各方程耦合。
- 每个 [[concepts/轨道]] $r_j = r_j(t)$ 只有在 [[concepts/存在性与唯一性定理]] 的条件下才有局部的存在唯一性保证。
- 求解 N 体问题的一般策略不是逐条积分轨道，而是构造[[concepts/系统宏观量]]（总质量、重心、总动量、总角动量、总动能、总势能）并考察[[concepts/平衡方程]]与[[concepts/守恒律]]。

## 特例

当 $N$ 体表示太阳与 $N-1$ 个行星，且力取引力形式时，即得到[[concepts/行星运动]]模型。