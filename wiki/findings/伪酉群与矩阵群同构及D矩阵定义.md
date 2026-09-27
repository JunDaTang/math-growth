---
type: finding
title: 伪酉群与矩阵群的同构及 D 矩阵定义
source: "[[10-数学指南实用数学手册--8-393-伪酉几何--1bvhqoc]]"
confidence: high
replicated: null
tags: [数学, 矩阵群, 同构]
related: [伪酉群, 伪正交群, 伪酉空间]
sources: ["数学指南_实用数学手册/3.9.3 伪酉几何.md"]
created: 2026-09-27
updated: 2026-09-27
---

# 伪酉群与矩阵群的同构及 D 矩阵定义

## 同构

取固定法正交基 $e_1, \cdots, e_n$ 并令 $(e_j, e_k) := \delta_{jk}$；对线性算子 $A: X \to X$ 相伴矩阵 $\mathscr{A} := (a_{jk})$，$a_{jk} := (e_j, A e_k)$。则复情形下的映射 $A \mapsto A$ 诱导群同构

$$
U(n-m, m; X) \simeq U(n-m, m) \quad \text{和} \quad SU(n-m, m; X) \simeq SU(n-m, m);
$$

实情形下有

$$
O(n-m, m; X) \simeq O(n-m, m) \quad \text{和} \quad SO(n-m, m; X) \simeq SO(n-m, m).
$$

## 矩阵群的定义

群 $U(n-m, m)$ 由满足

$$
\mathcal{A}^{*} \mathcal{D}_{n-m, m} \mathcal{A} = \mathcal{D}_{n-m, m}
$$

的 $n \times n$ 矩阵 $\mathcal{A}$ 组成，其中

$$
\mathcal{D}_{n-m, m} := \left( \begin{array}{cc} I_{n-m} & O \\ O & -I_m \end{array} \right),
$$

$I_r$ 为 $r \times r$ 单位矩阵。满足 $\det A = 1$ 的矩阵构成 $SU(n-m, m)$；$O(n-m,m)$（分别地 $SO(n-m,m)$）由 $U(n-m,m)$（分别地 $SU(n-m,m)$）中的实矩阵组成。

## 备注

算子相伴矩阵在符号上原文用 $\mathscr{A}$，而定义矩阵群时用 $\mathcal{A}$，属于记号混用（见 [[393节伪酉群记号n与m混用及定义式讹误]]）；此外定义矩阵 $\mathcal{D}_{n-m,m}$ 在同一节中另有一处写作 $\mathcal{D}_{n-m}$。

## Related
- [[findings/伪酉群与特殊伪酉群定义及维数]]
