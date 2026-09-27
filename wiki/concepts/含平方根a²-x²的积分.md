---
type: concept
title: 含平方根 √(a² - x²) 的积分
created: 2026-09-27
updated: 2026-09-27
tags: [积分, 不定积分, 无理函数, 圆]
related: [10-数学指南实用数学手册--9-095-不定积分表--1ced2rn, 无理函数的积分, 含平方根x²+a²的积分, 含平方根ax+b的积分]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表.md"]
---

# 含平方根 √(a² - x²) 的积分

0.9.5.2 节第五组，条目 147–174。根式为圆型 $Q = a^2 - x^2$，其有效范围为 $|x| \le a$。

## 记号

$$
Q = a^2 - x^2
$$

## 条目结构

| 条目 | 形态 | 结果标志 |
|---|---|---|
| 147–150 | $\sqrt{Q}$ 与 $x^k\sqrt{Q}$ | 含 $x\sqrt{Q}$ 与 $\arcsin(x/a)$ |
| 151–153 | $\sqrt{Q}/x^k$ | 含 $\ln\frac{a+\sqrt{Q}}{x}$ 或 $\arcsin(x/a)$ |
| 154–157 | $x^k/\sqrt{Q}$ | 含 $\arcsin(x/a)$ |
| 158–160 | $1/(x^k\sqrt{Q})$ | 含 $\ln\frac{a+\sqrt{Q}}{x}$ |
| 161–167 | $\sqrt{Q^3}$ 系列 | 含 $\arcsin(x/a)$ |
| 168–171 | $1/\sqrt{Q^3}$ 系列 | 含 $x/\sqrt{Q}$ 与 $\arcsin(x/a)$ |
| 172–174 | $1/(x^k\sqrt{Q^3})$ | 含 $\ln\frac{a+\sqrt{Q}}{x}$ |

## 代表公式

$$
\int \sqrt{Q}\,\mathrm{d}x = \frac{1}{2}\left(x\sqrt{Q} + a^2 \arcsin \frac{x}{a}\right) = \frac{1}{2}\left(x\sqrt{Q} + a^2 \arcsin \frac{x}{a}\right)
$$

$$
\int \frac{\mathrm{d}x}{\sqrt{Q}} = \arcsin \frac{x}{a}, \qquad
\int x\sqrt{Q}\,\mathrm{d}x = -\frac{1}{3}\sqrt{Q^3}
$$

$$
\int \frac{\mathrm{d}x}{x\sqrt{Q}} = -\frac{1}{a}\ln \frac{a+\sqrt{Q}}{x}, \qquad
\int \frac{\mathrm{d}x}{x^2\sqrt{Q}} = -\frac{\sqrt{Q}}{a^2 x}
$$

$$
\int \frac{\mathrm{d}x}{\sqrt{Q^3}} = \frac{x}{a^2\sqrt{Q}}, \qquad
\int \frac{x\,\mathrm{d}x}{\sqrt{Q^3}} = \frac{1}{\sqrt{Q}}
$$

$$
\int \frac{x^3\mathrm{d}x}{\sqrt{Q^3}} = \sqrt{Q} + \frac{a^2}{Q}
$$

$\arcsin(x/a)$ 与 $\ln\frac{a+\sqrt{Q}}{x}$ 是本组的两类结果函数：前者出现在分子不含 $x$ 的负幂或含 $x$ 的正幂条目中，后者出现在分母含 $x$ 的条目中。这与 [[concepts/含平方根x²+a²的积分]] 中出现 $\operatorname{arsinh}$ 与 $\ln\frac{a+\sqrt{Q}}{x}$ 的分工方式平行。

## 已知编号与转写疑点

- 条目 174（$\int \mathrm{d}x/(x^3 Q^3)$）与条目 175（$\int \sqrt{Q}\,\mathrm{d}x$，属下一组）在原文中未标编号。
- 条目 167（$\int \sqrt{Q^3}/x^3\,\mathrm{d}x$）中间的项在原文中写作 $-\frac{\sqrt{3\sqrt{Q}}}{2}$，与同族条目 165、166 的形式不协调。
- 条目 171（$\int x^3\mathrm{d}x/\sqrt{Q^3}$）的结果 $\sqrt{Q} + \frac{a^2}{Q}$ 中第二项的幂次与同族条目 169、170 的形式不协调。

均记录于 [[queries/095节首段公式转写疑误汇总]]；编号问题见 [[findings/095节首段条目编号缺号与重号]]。

## 相关页面

- [[concepts/无理函数的积分]]、[[concepts/含平方根x²+a²的积分]]
