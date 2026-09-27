---
type: query
title: 7.2.2.1 节 JOR 与 SOR 公式中的 E 是否为单位矩阵且未加定义？
created: 2026-09-28
updated: 2026-09-28
tags: [数值线性代数, 松弛法, 记号一致性]
related: [JOR方法, SOR逐次超松弛方法, 经典迭代法, 松弛因子与最优松弛因子]
sources: ["数学指南_实用数学手册/7.2.2 线性方程组的迭代法.md"]
---

# 7.2.2.1 节 JOR 与 SOR 公式中的 E 是否为单位矩阵且未加定义？

## 问题

源文 7.2.2.1 节在推导 JOR 时写出

$$
x^{(k+1)} = x^{(k)} + \omega\left[D^{-1}(L+U)x^{(k)} - D^{-1}b - x^{(k)}\right] = \left[(1-\omega)E + \omega D^{-1}(L+U)\right]x^{(k)} - \omega D^{-1}b,
$$

并在框出的迭代矩阵中再次使用 $E$：

$$
T_{\mathrm{JOR}}(\omega) := (1-\omega)E + \omega D^{-1}(L+U).
$$

## 疑点

1. **$E$ 在本节未定义**：7.2.2 节通篇仅定义了 $L$、$U$、$D$（以及 $T_{\mathrm{J}}、T_E、T_{\mathrm{JOR}}、T_{\mathrm{SOR}}、c_E、c_{\mathrm{JOR}}、c_{\mathrm{SOR}}$、$C$、$M$、$K$），没有给出 $E$ 的定义。
2. **按上下文推断**：由第一式中 $x^{(k)} - \omega x^{(k)} = (1-\omega)x^{(k)}$ 的合并过程可知，$E$ 应为**单位矩阵**。
3. **记号冲突风险**：本 wiki 中 $T_E$ 已用于表示高斯-赛德尔（单步）方法的迭代矩阵，下标 $E$ 与符号 $E$ 在同一小节内并存，容易混淆；原书是否在别处定义了 $E$（例如 Einheitsmatrix 的首字母），需要核对。
4. **SOR 公式中未出现 $E$**：SOR 的迭代矩阵写作 $(D-\omega L)^{-1}[(1-\omega)D + \omega U]$，此处以 $D$ 而非 $E$ 参与，形式上自洽；两支推广的记法不统一。

## 影响

若 $E$ 不是单位矩阵或另有定义，则 $T_{\mathrm{JOR}}(\omega)$ 及其 $\omega=1$ 退化为 $T_{\mathrm{J}}$ 的结论都不成立。就目前证据看，$E$ = 单位矩阵是最自然的解释，但源文缺少显式定义。

## 关联

- [[concepts/JOR方法]]
- [[concepts/SOR逐次超松弛方法]]
- [[findings/7221节经典迭代法族与收敛充分条件]]
- [[sources/10-数学指南实用数学手册--13-722-线性方程组的迭代法--rxhzax]]
