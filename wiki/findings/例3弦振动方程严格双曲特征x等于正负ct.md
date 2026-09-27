---
type: finding
title: 例 3：弦振动方程是严格双曲的，特征为 x = ±ct + 常数
tags: [例子, 分类, 波方程, 特征]
related: [波方程, 偏微分方程的分类, 特征-偏微分方程, 例2热导方程抛物特征t等于常数]
created: 2026-09-27
updated: 2026-09-27
sources: ["数学指南_实用数学手册/1.13.3 特征的作用.md"]
source: "10-数学指南实用数学手册--10-1133-特征的作用--113qzfn"
confidence: high
replicated: null
---

# 例 3：弦振动方程是严格双曲的，特征为 $x=\pm ct+\text{常数}$

《数学指南——实用数学手册》1.13.3.2 节的例 3。

## 内容

弦振动方程

$$
\frac{1}{c^2}u_{tt}-u_{xx} = 0
$$

有象征 $\mathcal{S}(\boldsymbol{\lambda}):=\frac{1}{c^2}\lambda_1^2-\lambda_2^2$。对于每个实数 $\lambda_1\neq 0$，方程 $\mathcal{S}(\boldsymbol{\lambda})=0$ 有两个实解 $\lambda_2$。因而弦振动方程是**严格双曲的**。

特征的方程是 $\psi(x,t)=0$。函数 $\psi$ 作为方程

$$
\frac{1}{c^2}\psi_t^2-\psi_x^2 = 0
$$

的解而得到。解族 $\psi=\pm ct-x+\text{常数}$ 相应于特征（图 1.164(b)）：

$$
x = \pm ct+\text{常数}.
$$

## 注

当 $c$ 增加时，这些特征接近热方程的特征 $t=\text{常数}$（见 [[例2热导方程抛物特征t等于常数]]）。

## 相关页面

- [[波方程]]
- [[偏微分方程的分类]]
- [[特征-偏微分方程]]