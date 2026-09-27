---
type: concept
title: arctan 的一般连分式
created: 2026-09-27
updated: 2026-09-27
tags: [连分数, arctan, 圆周率, 收敛速度]
related: [一般连分式, 莱布尼茨级数, 反三角函数的幂级数, 圆周率的计算史]
sources: ["数学指南_实用数学手册/2.7.7 对数 $ pi$ 的应用.md"]
---

# arctan 的一般连分式

《数学指南——实用数学手册》2.7.7 节给出：对于所有实数 $x$，有收敛的连分式

$$
\arctan x = \cfrac{x}{\lceil 1\rceil} + \cfrac{1^2\cdot x^2}{\lceil 3\rceil} + \cfrac{2^2\cdot x^2}{\lceil 5\rceil} + \cfrac{3^2\cdot x^2}{\lceil 7\rceil} + \dots \tag{2.92}
$$

与此不同，幂级数

$$
\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots \tag{2.93}
$$

仅当 $-1 \leqslant x \leqslant 1$ 时收敛。

## 与莱布尼茨级数的效率对比

若应用 $\frac{\pi}{4} = \arctan 1$：

- 在 (2.93) 中取 $x=1$ 可得 [[莱布尼茨级数]] (2.90)，它收敛得很慢；为将 $\pi$ 计算到第 7 位，大约要取 $10^6$ 项。
- 在 (2.92) 中取 $x=1$ 且计算 **9 项**，就可得到 $\pi$ 的具有相同精密度的近似值。

一般地有非常正则的表达式

$$
\frac{\pi}{4} = \cfrac{1}{\lceil 1\rceil} + \cfrac{1^2}{\lceil 3\rceil} + \cfrac{2^2}{\lceil 5\rceil} + \cfrac{3^2}{\lceil 7\rceil} + \dots \tag{2.94}
$$

该连分式是 [[一般连分式]] 的一个具体实例。
