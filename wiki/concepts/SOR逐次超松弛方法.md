---
type: concept
title: SOR 逐次超松弛方法
created: 2026-09-28
updated: 2026-09-28
tags: [数值线性代数, 迭代法, 松弛法, SOR]
related: [经典迭代法, 高斯-赛德尔方法, JOR方法, 松弛因子与最优松弛因子, 谱半径收敛判据]
sources: ["数学指南_实用数学手册/7.2.2 线性方程组的迭代法.md"]
---

# SOR 逐次超松弛方法

## 定义

SOR（successive overrelaxation，逐次超松弛）是[[concepts/高斯-赛德尔方法]]（单步方法）的松弛推广。源文 7.2.2.1 节给出：

$$
\begin{aligned}
x^{(k+1)} &= (D - \omega L)^{-1}\left[(1 - \omega)D + \omega U\right]x^{(k)} - \omega(D - \omega L)^{-1}b, \\
T_{\mathrm{SOR}}(\omega) &:= (D - \omega L)^{-1}\left[(1 - \omega)D + \omega U\right], \qquad c_{\mathrm{SOR}} := -\omega(D - \omega L)^{-1}b.
\end{aligned}
$$

即不动点迭代元素为

$$
\boxed{T_{\mathrm{SOR}}(\omega) := (D - \omega L)^{-1}[(1 - \omega)D + \omega U], \qquad c_{\mathrm{SOR}} := -\omega(D - \omega L)^{-1}b.}
$$

## 与高斯-赛德尔方法的关系

非松弛情形（$\omega = 1$）下，$T_{\mathrm{SOR}}(1) = (D - L)^{-1}[0 \cdot D + U] = (D-L)^{-1}U = T_E$、$c_{\mathrm{SOR}}(1) = -(D-L)^{-1}b$，除符号约定外即回到单步方法的不动点迭代单元。这为「SOR 是单步方法的松弛推广」提供了代数说明。

## 松弛因子的作用

- $\omega > 1$：**超松弛**（overrelaxation）；
- $\omega \leqslant 1$：**低松弛**（underrelaxation）。

最优松弛因子 $\omega_{opt}$ 的选取要使得 $\rho(T_{\mathrm{SOR}}(\omega))$ 最小。源文强调：由于系数矩阵 $A$ 有不同的性质，选取 $\omega_{opt}$ 的方法理论上也有不同的可能性。详见[[concepts/松弛因子与最优松弛因子]]。

与 [[concepts/JOR方法]] 的对照：JOR 对**组合步**做松弛，SOR 对**单步**做松弛；SOR 的迭代矩阵中出现 $(D - \omega L)^{-1}$，需要每次迭代求解一个下三角方程组。

## 相关联方法

- [[concepts/经典迭代法]]
- [[concepts/高斯-赛德尔方法]]
- [[concepts/JOR方法]]
- [[sources/10-数学指南实用数学手册--13-722-线性方程组的迭代法--rxhzax]]
