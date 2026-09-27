---
type: concept
title: 含平方根 √(x² + a²) 的积分
created: 2026-09-27
updated: 2026-09-27
tags: [积分, 不定积分, 无理函数, 反双曲函数]
related: [10-数学指南实用数学手册--9-095-不定积分表--1ced2rn, 无理函数的积分, 含平方根a²-x²的积分, 反双曲函数记号, 双曲正弦]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表.md"]
---

# 含平方根 √(x² + a²) 的积分

0.9.5.2 节第六组，条目 175–180，也是本段（条目 1–180）的最后一组。根式为 $Q = x^2 + a^2$，对全体实数有定义。

## 记号

$$
Q = x^2 + a^2
$$

## 条目与公式

$$
\int \sqrt{Q}\,\mathrm{d}x = \frac{1}{2}\left(x\sqrt{Q} + a^2 \operatorname{arsinh} \frac{x}{a}\right)
= \frac{1}{2}\left[x\sqrt{Q} + a^2(\ln(x+\sqrt{Q}) - \ln a)\right]
$$

$$
\int x\sqrt{Q}\,\mathrm{d}x = \frac{1}{3}\sqrt{Q^3}
$$

$$
\int x^2\sqrt{Q}\,\mathrm{d}x = \frac{x}{4}\sqrt{Q^3} - \frac{a^2}{8}\left(x\sqrt{Q} + a^2\operatorname{arsinh}\frac{x}{a}\right)
= \frac{x}{4}\sqrt{Q^3} - \frac{a^2}{8}\left[x\sqrt{Q} + a^2(\ln(x+\sqrt{Q}) - \ln a)\right]
$$

$$
\int x^3\sqrt{Q}\,\mathrm{d}x = \frac{\sqrt{Q^5}}{5} - \frac{a^2\sqrt{Q^3}}{3}
$$

$$
\int \frac{\sqrt{Q}}{x}\mathrm{d}x = \sqrt{Q} - a\ln \frac{a+\sqrt{Q}}{x}
$$

$$
\int \frac{\sqrt{Q}}{x^2}\mathrm{d}x = -\frac{\sqrt{Q}}{x} + \operatorname{arsinh}\frac{x}{a} = -\frac{\sqrt{Q}}{x} + \ln(x+\sqrt{Q}) - \ln a
$$

## 与第五组的对照

本组与 [[concepts/含平方根a²-x²的积分]]（$Q = a^2-x^2$）结构对称：$\arcsin(x/a)$ 的位置在 $x^2+a^2$ 情形由 $\operatorname{arsinh}(x/a)$ 取代。原文对条目 175、177、180 同时给出 $\operatorname{arsinh}$ 与对数两种写法，并明确 $\operatorname{arsinh}\frac{x}{a} = \ln(x+\sqrt{Q}) - \ln a$，这条恒等式把 $\operatorname{arsinh}$ 归到本手册自身的反双曲函数记法体系（见 [[concepts/反双曲函数记号]]、[[concepts/双曲正弦]]）。

本组条目在原文中多数未标编号：175 与 180 在公式前均无编号，仅 176–179 带号。见 [[findings/095节首段条目编号缺号与重号]]。

## 相关页面

- [[concepts/无理函数的积分]]、[[concepts/含平方根a²-x²的积分]]、[[concepts/反双曲函数记号]]
