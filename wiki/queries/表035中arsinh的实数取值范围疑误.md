---
type: query
title: 表 0.35 中 arsinh 的实数取值范围疑误
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 微分表, 转写疑误, 待核对]
related: [一阶导数表, 初等函数, 反函数求导法则]
sources: ["数学指南_实用数学手册/0.8 函数的微分表.md"]
---

# 表 0.35 中 arsinh 的实数取值范围疑误

## 问题

《数学指南——实用数学手册》表 0.35（[[一阶导数表]]）中，$\operatorname{arsinh} x$ 一行给出：

| 函数 | 导数 | 对实数的取值范围 | 对复数的取值范围 |
|---|---|---|---|
| $\operatorname{arsinh} x$ | $\frac{1}{\sqrt{1 + x^{2}}}$ | $-1 < x < 1$ | $|x| < 1$ |

## 疑点

1. **实数栏**：$\operatorname{arsinh} x = \ln\left(x + \sqrt{x^{2}+1}\right)$ 在整个实轴上有定义，其导数 $\frac{1}{\sqrt{1+x^{2}}}$ 也在整个实轴上存在，因此实数范围应为 $x \in \mathbb{R}$，而非 $-1 < x < 1$。
2. **复数栏**：$\frac{1}{\sqrt{1+x^{2}}}$ 的解析分支的奇异点位于 $x = \pm \mathrm{i}$，用 $|x| < 1$ 描述复数域成立范围过于狭窄，且与同表中 $\arctan x$ 用 $|\operatorname{Im} x| < 1$ 的写法不协调。

## 可能的解释

- 该行数值范围可能是排版或转写时与相邻行（$\arcsin x$、$\arccos x$ 的 $-1 < x < 1$ 与 $|x| < 1$）串行所致。
- 也可能是手册原文如此，属于原书的印刷问题。

## 待核对

需要核对《数学指南——实用数学手册》纸质版或德文原版（Teubner-Taschenbuch der Mathematik）0.8.1 节表 0.35 的 $\operatorname{arsinh}$ 行，确认是转写错误还是原书错误。同时应检查同一表格中其余反双曲函数行（$\operatorname{arcosh}$、$\operatorname{artanh}$、$\operatorname{arcoth}$）的范围栏目是否也受影响。