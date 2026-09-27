---
type: finding
title: 表 0.20 中 tanh 与 coth 的零点极点互换
source: "10-数学指南实用数学手册--27-0211-双曲函数-tanh-x-和-coth-x--1tmwzib"
tags: [数学, 双曲函数, 零点, 极点]
related: [表020双曲函数与三角函数的零点与极点, 双曲正切, 双曲余切, 双曲函数与三角函数的零点与极点]
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
sources: ["数学指南_实用数学手册/0.2.11 双曲函数 $ tanh x$ 和 $ coth x$.md"]
---

# 表 0.20 中 tanh 与 coth 的零点极点互换

## 结果

在表 0.20 中，$\tanh x$ 的零点集 $\{\pi k \mathrm{i}\}$ 恰等于 $\coth x$ 的极点集，而 $\tanh x$ 的极点集 $\{(\pi k + \pi/2)\mathrm{i}\}$ 恰等于 $\coth x$ 的零点集。

## 依据

- $\tanh x = \sinh x / \cosh x$：零点来自分子 $\sinh$（$\pi k \mathrm{i}$），极点来自分母 $\cosh$（$(\pi k + \pi/2)\mathrm{i}$）；
- $\coth x = \cosh x / \sinh x$：分子分母互换，于是零点与极点也随之互换；
- 这一互换是 $\coth x = 1/\tanh x$ 的必然结果。

## 直接证据 vs. 推断

表 0.20 的**表格数值**是直接证据；「互换源于商的分子分母对调」是**推断**，但它与定义式精确吻合，可视为定义域限制的直接改写。

## 关联

该互换同时解释了两函数的定义域限制（见 [[双曲正切]]、[[双曲余切]]），并与三角函数侧 $\tan$、$\cot$ 的互换结构平行（见 [[双曲函数与三角函数的零点与极点]]）。

## Related
- [[findings/0211节双曲函数定义域由分母零点决定]]
