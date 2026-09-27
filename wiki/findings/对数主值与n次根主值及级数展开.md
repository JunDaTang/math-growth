---
type: finding
title: 对数主值与 n 次根主值及其级数展开（源文档例 1、例 2）
created: 2026-09-27
updated: 2026-09-27
tags: [复变函数, 多值函数, 主值, 幂级数]
related: [对数主值, 分支点, 对数黎曼面, 全纯函数]
sources: ["数学指南_实用数学手册/1.14.11 共形映射的例子.md"]
source: "10-数学指南实用数学手册--13-11411-共形映射的例子--18583k5"
confidence: medium
replicated: null
---

# 对数主值与 n 次根主值及其级数展开

## 内容

**对数的主值**：令 $w = R\mathrm{e}^{\mathrm{i}\psi}$，$-\pi < \psi \leqslant \pi$，$w \neq 0$，定义

$$
\ln w := \ln R + \mathrm{i}\psi,
$$

它对应 [[findings/对数黎曼面为无穷圈楼梯]] 中 $B_0$ 片上的 $\operatorname{Ln} w$（要点是幅角取在 $-\pi < \psi \leqslant \pi$）。

**n 次根主值**：对 $w = R\mathrm{e}^{\mathrm{i}\psi}$（$-\pi < \psi \leqslant \pi$）、$n = 2,3,\cdots$，主值定义为 $\sqrt[n]{R}\,\mathrm{e}^{\mathrm{i}\psi/n}$。

**例 1**：对所有满足 $|z| < 1$ 的 $z \in \mathbb{C}$，

$$
\ln(1 + z) = z - \frac{z^{3}}{3} + \frac{z^{5}}{5} - \dots
$$

**例 2**：对所有满足 $|z| < 1$ 的 $z \in \mathbb{C}$，

$$
\sqrt[n]{1 + z} = 1 + \alpha z + (\alpha/2) z^{2} + (\alpha/3) z^{3} + \dots, \qquad \alpha = 1/n
$$

（在 $n$ 次根主值的意义下）。

## 证据评估与保留意见

主值定义本身是标准的、证据强。但两个级数展开式**与标准结果不符**：$\ln(1+z)$ 的 Taylor 级数为 $z - z^2/2 + z^3/3 - \cdots$，而 $(1+z)^{1/n}$ 的二项级数系数应为 $\alpha(\alpha-1)/2$ 等。源文档中的幂次与系数疑为印刷或转录错误，故本条置信度标记为 medium，详见 [[queries/11411节例1与例2级数展开式疑有误]]。

## 出处

《数学指南——实用数学手册》1.14.11.7。