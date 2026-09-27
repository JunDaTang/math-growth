---
type: concept
title: LR分解
tags: [矩阵分解, 数值线性代数, 消元法]
related: [高斯算法, 线性方程组直接法, 主元选取策略, 线性方程组的条件数]
created: 2026-09-28
updated: 2026-09-28
sources: ["数学指南_实用数学手册/7.2.1 线性方程组——直接法.md"]
---

# LR分解

## 定义

对给定矩阵 $A$，高斯算法通过适当交换行产生两个矩阵：对角线为 1 的下三角矩阵 $L$ 与上三角矩阵 $R$。记消元后最后形式的矩阵元素为 $r_{ik}$、常数列为 $c_i$，左下三角零元素（乘子）为 $l_{ik}$（$i > k$），则

$$
R := \begin{pmatrix}
r_{11} & r_{12} & r_{13} & \dots & r_{1n} \\
0 & r_{22} & r_{23} & \dots & r_{2n} \\
0 & 0 & r_{33} & \dots & r_{3n} \\
\vdots & \vdots & \vdots & & \vdots \\
0 & 0 & 0 & \dots & r_{nn}
\end{pmatrix}, \quad
L := \begin{pmatrix}
1 & 0 & 0 & \dots & 0 \\
l_{21} & 1 & 0 & \dots & 0 \\
l_{31} & l_{32} & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & & \vdots \\
l_{n1} & l_{n2} & l_{n3} & \dots & 1
\end{pmatrix},
$$

并以算法中执行行变换的置换矩阵 $P$ 联系为

$$
P \cdot A = L \cdot R \quad (\mathrm{LR}\ \text{分解}).
$$

> 源文档此式右端排作 $L \cdot A$，应为 $L \cdot R$，见 [[queries/721节置换矩阵恒等式PA等于LA疑为PA等于LR]]。

## 与求解方程组的联系

$$
P(Ax + b) = PAx + Pb = LRx + Pb = -Lc + Pb = 0, \quad \text{其中 } Rx = -c,
$$

即可写成三步：

$$
\begin{array}{ll}
1. & PA = LR \quad (\mathrm{LR}\ \text{分解}), \\
2. & Lc - Pb = 0 \quad (\text{向前代换} \rightarrow c), \\
3. & Rx + c = 0 \quad (\text{逆代换} \rightarrow x).
\end{array}
$$

对同一 $A$ 与不同的 $b$ 求解时该格式特别有用：$A$ 只需分解一次。

## 计算量

$$
Z_{\mathrm{LR}} = \frac{n^3 - n}{3} \quad (\text{乘除法}), \qquad Z_{\mathrm{VR}} = n^2 \quad (\text{向前与回代}),
$$

合计即 [[高斯算法]] 的 $Z_{\mathrm{Gauss}} = \frac{1}{3}(n^3 + 3n^2 - n)$。

## 用途

- **行列式计算**：$\det A = (-1)^V \prod_{k=1}^{n} r_{kk}$，其中 $\det L = 1$、$\det R = \prod_k r_{kk}$、$\det P = (-1)^V$（$V$ 为行交换总次数）。
- **三对角特例**：$L$、$R$ 退化为二对角线矩阵，见 [[三对角线方程组]]。
- 与对称正定情形下的 [[楚列斯基分解]]（$A = LL^{\mathrm{T}}$）对照：后者计算量约为 $LR$ 分解的一半。

## 稳定性的前提

$LR$ 分解的可靠性依赖主元选取，见 [[主元选取策略]] 与 [[对角占优]]。