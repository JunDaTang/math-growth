---
type: concept
title: 含三次函数 a³ ± x³ 的积分
created: 2026-09-27
updated: 2026-09-27
tags: [积分, 不定积分, 有理函数, 三次函数]
related: [10-数学指南实用数学手册--9-095-不定积分表--1ced2rn, 有理函数的积分, 含四次函数a⁴±x⁴的积分, 积分递推公式, 不定积分表的记号与适用范围约定]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表.md"]
---

# 含三次函数 a³ ± x³ 的积分

0.9.5.1 节第五组，条目 73–86。分母为 $K = a^3 \pm x^3$。

## 记号

$$
K = a^3 \pm x^3
$$

原文说明重号的读法：上符号表示 $K = a^3 + x^3$，下符号表示 $K = a^3 - x^3$。

## 基本积分（条目 73）

$$
\int \frac{\mathrm{d}x}{K} = \pm \frac{1}{6a^2}\ln \frac{(a \pm x)^2}{a^2 \mp ax + x^2} + \frac{1}{a^2\sqrt{3}} \arctan \frac{2x \mp a}{a\sqrt{3}}
$$

结果由对数项与反正切项相加构成：$a^3 \pm x^3$ 在实数域分解为一个一次因式与一个不可约二次因式，故基本积分同时含 $\ln$ 与 $\arctan$。这与 [[concepts/含一般二次函数的积分]] 中 $D<0$ 时的对数—反正切结构同源。$a\sqrt{3}$ 的出现来自二次因式 $a^2 \mp ax + x^2$ 的判别式为 $-3a^2$。

## 条目结构与归约终点

| 条目 | 形态 | 归约目标 |
|---|---|---|
| 73 | $\int \mathrm{d}x/K$ | 基本积分 |
| 74 | $\int \mathrm{d}x/K^2$ | 参看 73 |
| 75 | $\int x\,\mathrm{d}x/K$ | 独立给出对数—反正切式 |
| 76 | $\int x\,\mathrm{d}x/K^2$ | 参看 75 |
| 77–78 | $\int x^2\mathrm{d}x/K^k$ | 直接给出 $\ln K$ 或 $1/K$ |
| 79–80 | $\int x^3\mathrm{d}x/K^k$ | 参看 73 |
| 81–82 | $\int \mathrm{d}x/(xK^k)$ | 含 $\ln(x^3/K)$ |
| 83–86 | $\int \mathrm{d}x/(x^2 K^k)$、$\int \mathrm{d}x/(x^3 K^k)$ | 参看 73 或 75 |

$$
\int \frac{x\,\mathrm{d}x}{K} = \frac{1}{6a}\ln \frac{a^2 \mp ax + x^2}{(a \pm x)^2} + \frac{1}{a\sqrt{3}}\arctan \frac{2x \mp a}{a\sqrt{3}}
$$

$$
\int \frac{x^2 \mathrm{d}x}{K} = \pm \frac{1}{3}\ln K, \qquad
\int \frac{x^2 \mathrm{d}x}{K^2} = \mp \frac{1}{3K}
$$

$$
\int \frac{\mathrm{d}x}{xK} = \frac{1}{3a^3}\ln \frac{x^3}{K}, \qquad
\int \frac{\mathrm{d}x}{xK^2} = \frac{1}{3a^3K} + \frac{1}{3a^6}\ln \frac{x^3}{K}
$$

## 已知转写疑点

条目 83 与 84 中的第二项在原文中写作 $\mp \frac{1}{a^3}\frac{x\,\mathrm{d}x}{K}$ 与 $\mp \frac{4}{3a^6}\int\frac{x\,\mathrm{d}x}{K}$，前者缺少积分号，形制与后者不一致。记录见 [[queries/095节首段公式转写疑误汇总]]。

## 相关页面

- [[concepts/含四次函数a⁴±x⁴的积分]]、[[concepts/有理函数的积分]]、[[concepts/积分递推公式]]
