---
type: concept
title: 含平方根 √(ax + b) 的积分
created: 2026-09-27
updated: 2026-09-27
tags: [积分, 不定积分, 无理函数, 根式]
related: [10-数学指南实用数学手册--9-095-不定积分表--1ced2rn, 无理函数的积分, 含平方根a²-x²的积分, 积分递推公式]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表.md"]
---

# 含平方根 √(ax + b) 的积分

0.9.5.2 节第三组，条目 111–135。根式为线性式的平方根。

## 记号

$$
L = ax + b
$$

## 条目结构

| 子组 | 条目 | 形态 |
|---|---|---|
| $\sqrt{L}$ 的正幂 | 111–113 | $\int \sqrt{L}\,\mathrm{d}x$、$\int x\sqrt{L}\,\mathrm{d}x$、$\int x^2\sqrt{L}\,\mathrm{d}x$ |
| $1/\sqrt{L}$ | 114–116 | $\int \mathrm{d}x/\sqrt{L}$、$\int x\,\mathrm{d}x/\sqrt{L}$、$\int x^2\mathrm{d}x/\sqrt{L}$ |
| 分母含 $x$ | 117–121 | 117 按 $b>0$、$b<0$ 分两支；118–121 回指 117 |
| $\sqrt{L^3}$ | 122–125 | 122–124 为幂次表，125 含 $\int \mathrm{d}x/(x\sqrt{L})$ |
| $1/\sqrt{L^3}$ | 126–129 | 分母含 $x$ 的条目回指 117 |
| $L^{\pm n/2}$ 通用式 | 130–135 | 统一覆盖前述具体幂次 |

## 两个标志性公式

$$
\int \frac{\mathrm{d}x}{x\sqrt{L}} =
\begin{cases}
\dfrac{1}{\sqrt{b}}\ln \dfrac{\sqrt{L}-\sqrt{b}}{\sqrt{L}+\sqrt{b}}, & b > 0, \\[6pt]
\dfrac{2}{\sqrt{-b}}\arctan \sqrt{\dfrac{L}{-b}}, & b < 0.
\end{cases}
$$

$$
\int \frac{\sqrt{L}}{x}\mathrm{d}x = 2\sqrt{L} + b\int \frac{\mathrm{d}x}{x\sqrt{L}}
$$

条目 117 是 118–121、125、128、129 的共同归约目标，都以"（参看第 117 个积分）"标注。它的两种分支体现了 $\sqrt{ax+b}$ 在 $b>0$ 与 $b<0$ 时根式零点位置不同：前者可用 $\operatorname{artanh}$ 型的对数式，后者需用 $\arctan$。

## 通用幂次式

$$
\int L^{\pm n/2}\,\mathrm{d}x = \frac{2L^{(2 \pm n)/2}}{a(2 \pm n)}
$$

$$
\int x L^{\pm n/2}\,\mathrm{d}x = \frac{2}{a^2}\left(\frac{L^{(4 \pm n)/2}}{4 \pm n} - \frac{bL^{(2 \pm n)/2}}{2 \pm n}\right)
$$

$$
\int x^2 L^{\pm n/2}\,\mathrm{d}x = \frac{2}{a^3}\left(\frac{L^{(6 \pm n)/2}}{6 \pm n} - \frac{2bL^{(4 \pm n)/2}}{4 \pm n} + \frac{b^2 L^{(2 \pm n)/2}}{2 \pm n}\right)
$$

$$
\int \frac{L^{n/2}\mathrm{d}x}{x} = \frac{2L^{n/2}}{n} + b\int \frac{L^{(n-2)/2}}{x}\mathrm{d}x, \qquad
\int \frac{\mathrm{d}x}{xL^{n/2}} = \frac{2}{(n-2)bL^{(n-2)/2}} + \frac{1}{b}\int \frac{\mathrm{d}x}{xL^{(n-2)/2}}
$$

## 已知转写疑点

条目 122–124 的标签与被积函数不匹配：条目 123 的标签写作 $\int x^2\sqrt{L^3}\,\mathrm{d}x$，但给出的结果 $\frac{2}{35a^2}(5\sqrt{L^7} - 7b\sqrt{L^5})$ 对应 $\int x\sqrt{L^3}\,\mathrm{d}x$；条目 124 才是 $x^2$ 的对应式。此外条目 132 的第一个幂次在原文中写作 $L^{(4\pm n)}/2$，与同式第二、三项的 $L^{(4\pm n)/2}$、$L^{(2\pm n)/2}$ 不一致。记录见 [[queries/095节首段公式转写疑误汇总]]。

## 相关页面

- [[concepts/无理函数的积分]]、[[findings/095节首段根式积分幂次统一式130至135]]、[[concepts/积分递推公式]]
