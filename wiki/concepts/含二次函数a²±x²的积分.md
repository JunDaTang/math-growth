---
type: concept
title: 含二次函数 a² ± x² 的积分
created: 2026-09-27
updated: 2026-09-27
tags: [积分, 不定积分, 有理函数, 重号约定]
related: [10-数学指南实用数学手册--9-095-不定积分表--1ced2rn, 含一般二次函数的积分, 有理函数的积分, 不定积分表的记号与适用范围约定, 反双曲函数记号]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表.md"]
---

# 含二次函数 a² ± x² 的积分

0.9.5.1 节第四组，条目 47–72。它把 [[concepts/含一般二次函数的积分]] 中 $Q = ax^2+bx+c$ 的特例 $Q = a^2 \pm x^2$ 抽出来，并用重号把 $a^2+x^2$ 与 $a^2-x^2$ 两种情形合并书写。

## 记号与辅助函数 P

$$
Q = a^2 \pm x^2
$$

$$
P = \begin{cases}
\arctan \dfrac{x}{a}, & \text{若取 “+”}, \\[6pt]
\operatorname{artanh} \dfrac{x}{a} = \dfrac{1}{2}\ln \dfrac{a+x}{a-x}, & \text{若取 “−” 且 } |x| < a, \\[6pt]
\operatorname{arcoth} \dfrac{x}{a} = \dfrac{1}{2}\ln \dfrac{x+a}{x-a}, & \text{若取 “−” 且 } |x| > a.
\end{cases}
$$

$P$ 把 $\arctan$、$\operatorname{artanh}$、$\operatorname{arcoth}$ 三个函数统一成一个符号，使得 47–50、66–68、72 等条目可以用单行书写。这里出现的反双曲函数记法见 [[concepts/反双曲函数记号]]。

## 条目结构

| 条目 | 形态 | 说明 |
|---|---|---|
| 47–50 | $\int \mathrm{d}x/Q^k$ | 47 为基本积分 $\frac{1}{a}P$；48–50 为 $Q^2$、$Q^3$ 与 $n+1$ 次的一般递推 |
| 51–54 | $\int x\,\mathrm{d}x/Q^k$ | 结果为 $\mp$ 号下的 $\ln Q$ 或 $1/Q^{k-1}$ |
| 55–58 | $\int x^2\mathrm{d}x/Q^k$ | 含 $\pm x$ 与 $\pm aP$（或 $\pm \int \mathrm{d}x/Q^n$） |
| 59–62 | $\int x^3\mathrm{d}x/Q^k$ | 含 $\ln Q$ 与 $1/Q^{k-1}$ |
| 63–65 | $\int \mathrm{d}x/(xQ^k)$ | 对数形式 $\ln(x^2/Q)$ |
| 66–68 | $\int \mathrm{d}x/(x^2Q^k)$ | 含 $\mp P$ |
| 69–71 | $\int \mathrm{d}x/(x^3Q^k)$ | 含 $\mp \ln(x^2/Q)$ |
| 72 | $\int \mathrm{d}x/((b+cx)Q)$ | 一般分母 $(b+cx)Q$ |

## 重号约定

本组大量使用 $\pm$ 与 $\mp$：条目前半部分的 $\pm$ 与后半部分的 $\mp$ 方向相反，用以同时覆盖 $a^2+x^2$（上符号）与 $a^2-x^2$（下符号）两种情形。原文在条目 62 之后特别说明：第 50、54、58 个积分要求 $n \neq 0$，第 62 个要求 $n > 1$。

## 代表公式

$$
\int \frac{\mathrm{d}x}{Q} = \frac{1}{a}P
$$

$$
\int \frac{\mathrm{d}x}{Q^{n+1}} = \frac{x}{2na^2Q^n} + \frac{2n-1}{2na^2}\int \frac{\mathrm{d}x}{Q^n}
$$

$$
\int \frac{x^2 \mathrm{d}x}{Q^{n+1}} = \mp \frac{x}{2nQ^n} \pm \frac{1}{2n}\int \frac{\mathrm{d}x}{Q^n}
$$

$$
\int \frac{\mathrm{d}x}{xQ} = \frac{1}{2a^2}\ln \frac{x^2}{Q}
$$

$$
\int \frac{\mathrm{d}x}{(b+cx)Q} = \frac{1}{a^2c^2 \pm b^2}\left[c\ln(b+cx) - \frac{c}{2}\ln Q \pm \frac{b}{a}P\right]
$$

## 相关页面

- [[concepts/含一般二次函数的积分]]、[[concepts/有理函数的积分]]、[[concepts/积分递推公式]]、[[concepts/不定积分表的记号与适用范围约定]]
