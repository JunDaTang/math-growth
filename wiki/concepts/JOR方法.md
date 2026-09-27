---
type: concept
title: JOR方法（组合步松弛）
created: 2026-09-28
updated: 2026-09-28
tags: [数值线性代数, 迭代法, 松弛法, JOR]
related: [经典迭代法, 雅可比方法, SOR逐次超松弛方法, 松弛因子与最优松弛因子, 谱半径收敛判据]
sources: ["数学指南_实用数学手册/7.2.2 线性方程组的迭代法.md"]
---

# JOR方法（组合步松弛）

## 定义

JOR 是**组合步方法的松弛推广**。源文 7.2.2.1 节在说明松弛因子 $\omega \neq 1$ 的作用后指出：组合步方法产生 JOR 算法如下：

$$
\begin{aligned}
x^{(k+1)} &= x^{(k)} + \omega\left[D^{-1}(L + U)x^{(k)} - D^{-1}b - x^{(k)}\right] \\
&= \left[(1 - \omega)E + \omega D^{-1}(L + U)\right]x^{(k)} - \omega D^{-1}b.
\end{aligned}
$$

因此不动点迭代的元素为

$$
\boxed{T_{\mathrm{JOR}}(\omega) := (1 - \omega)E + \omega D^{-1}(L + U), \qquad c_{\mathrm{JOR}} := -\omega D^{-1}b.}
$$

其中修正项 $\omega[\cdot]$ 的形式是把[[concepts/雅可比方法]]的单步增量（即 $D^{-1}(L+U)x^{(k)} - D^{-1}b - x^{(k)}$）按因子 $\omega$ 放大或缩小。

## 与雅可比方法的关系

当 $\omega = 1$ 时，$T_{\mathrm{JOR}}(1) = 0 \cdot E + 1 \cdot D^{-1}(L+U) = D^{-1}(L+U) = T_{\mathrm{J}}$，即退化为雅可比方法。这为「JOR 是组合步方法的松弛推广」提供了直接的代数说明。

## 松弛因子的作用

当 $\omega > 1$ 时称为**超松弛**，当 $\omega \leqslant 1$ 时称为**低松弛**。$\omega_{opt}$ 的选取要使得谱半径 $\rho(T_{\mathrm{JOR}}(\omega))$ 最小；由于 $A$ 的性质不同，选取方法理论上也有不同的可能性。详见[[concepts/松弛因子与最优松弛因子]]。

源文未对 JOR 单独列出收敛的充分条件（对比雅可比方法的对角占优条件），其收敛性只能回到[[concepts/谱半径收敛判据]] $\rho(T_{\mathrm{JOR}}(\omega)) < 1$ 来判定。

## 记号说明

源文公式中出现的 $E$ 在 7.2.2 节中未给出显式定义；按上下文（$(1-\omega)E$ 与单位增量对应的写法）它应指单位矩阵。该记号问题记录于[[queries/7221节JOR与SOR公式中E记号未定义]]。

## 相关联方法

- [[concepts/经典迭代法]]
- [[concepts/雅可比方法]]
- [[concepts/SOR逐次超松弛方法]]
- [[sources/10-数学指南实用数学手册--13-722-线性方程组的迭代法--rxhzax]]
