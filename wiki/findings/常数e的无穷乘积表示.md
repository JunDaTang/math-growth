---
type: finding
title: 常数 e 的无穷乘积表示
created: 2026-09-27
updated: 2026-09-27
tags: [无穷乘积, 常数e, 特值]
related: [无穷乘积, sin-πx-的无穷乘积表示, 欧拉常数的无穷乘积表示, 10-数学指南实用数学手册--8-075-无穷乘积--do8tmf]
source: "[[10-数学指南实用数学手册--8-075-无穷乘积--do8tmf]]"
confidence: high
replicated: null
sources: ["数学指南_实用数学手册/0.7.5 无穷乘积.md"]
---

# 常数 e 的无穷乘积表示

《数学指南——实用数学手册》0.7.5 节「进一步的几个例子」的第四条用幂次逐步加深的无穷乘积表示常数 $\mathrm{e}$：

$$\left(\frac{2}{1}\right)\left(\frac{4}{3}\right)^{1/2}\left(\frac{6 \cdot 8}{5 \cdot 7}\right)^{1/4}\left(\frac{10 \cdot 12 \cdot 14 \cdot 16}{9 \cdot 11 \cdot 13 \cdot 15}\right)^{1/8} \cdots = \mathrm{e}$$

结构上的观察（依据源中写出的形式）：

- 第 $j$ 个因子的分子与分母各含 $2^{j-1}$ 个连续整数对，分子取偶数列并略有偏移、分母取奇数列，指数依次为 $1, 1/2, 1/4, 1/8, \dots$。
- 源中只给出结果 $\mathrm{e}$，未给出推导，也未给出收敛性说明。
- 与同节的 [[欧拉常数的无穷乘积表示]] 对照：两者都是把乘积的极限值写成与 $\mathrm{e}$ 有关的常数。
