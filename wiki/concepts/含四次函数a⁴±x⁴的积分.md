---
type: concept
title: 含四次函数 a⁴ ± x⁴ 的积分
created: 2026-09-27
updated: 2026-09-27
tags: [积分, 不定积分, 有理函数, 四次函数]
related: [10-数学指南实用数学手册--9-095-不定积分表--1ced2rn, 含三次函数a³±x³的积分, 有理函数的积分, 部分分式分解]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表.md"]
---

# 含四次函数 a⁴ ± x⁴ 的积分

0.9.5.1 节第六组，条目 87–94。分母为四次式 $a^4 \pm x^4$，按分子幂次 $x^0$ 到 $x^3$ 各给一条。

## 条目结构

| 条目 | 被积函数 |
|---|---|
| 87 | $\mathrm{d}x/(a^4+x^4)$ |
| 88 | $x\,\mathrm{d}x/(a^4+x^4)$ |
| 89 | $x^2\mathrm{d}x/(a^4+x^4)$ |
| 90 | $x^3\mathrm{d}x/(a^4+x^4)$ |
| 91 | $\mathrm{d}x/(a^4-x^4)$ |
| 92 | $x\,\mathrm{d}x/(a^4-x^4)$ |
| 93 | $x^2\mathrm{d}x/(a^4-x^4)$ |
| 94 | $x^3\mathrm{d}x/(a^4-x^4)$ |

## 代表公式

$$
\int \frac{\mathrm{d}x}{a^4+x^4} = \frac{1}{4a^3\sqrt{2}}\ln \frac{x^2+ax\sqrt{2}+a^2}{x^2-ax\sqrt{2}+a^2}
+ \frac{1}{2a^3\sqrt{2}}\left(\arctan\left(\frac{x\sqrt{2}}{a}+1\right) + \arctan\left(\frac{x\sqrt{2}}{a}-1\right)\right)
$$

$$
\int \frac{x\,\mathrm{d}x}{a^4+x^4} = \frac{1}{2a^2}\arctan \frac{x^2}{a^2}, \qquad
\int \frac{x^3\mathrm{d}x}{a^4+x^4} = \frac{1}{4}\ln(a^4+x^4)
$$

$$
\int \frac{\mathrm{d}x}{a^4-x^4} = \frac{1}{4a^3}\ln \frac{a+x}{a-x} + \frac{1}{2a^3}\arctan \frac{x}{a}
$$

$$
\int \frac{x^2 \mathrm{d}x}{a^4-x^4} = \frac{1}{4a}\ln \frac{a+x}{a-x} - \frac{1}{2a}\arctan \frac{x}{a}, \qquad
\int \frac{x^3\mathrm{d}x}{a^4-x^4} = -\frac{1}{4}\ln(a^4-x^4)
$$

分子为 $x$ 或 $x^3$ 的条目（88、90、92、94）是对数或反正切函数的简单复合，可由 $\mathrm{d}(x^2)$ 直接代换得到；分子为 $1$ 或 $x^2$ 的条目（87、89、91、93）需先把 $a^4 \pm x^4$ 配方为 $(x^2 \pm ax\sqrt{2} + a^2)(x^2 \mp ax\sqrt{2} + a^2)$（$a^4+x^4$ 情形）或 $(a^2+x^2)(a^2-x^2)$（$a^4-x^4$ 情形），再作部分分式分解。

## 相关页面

- [[concepts/含三次函数a³±x³的积分]]、[[concepts/部分分式分解]]、[[concepts/有理函数的积分]]
