---
type: finding
title: 圆周内部面积由极坐标二重积分算得 πR²
source: "[[10-数学指南实用数学手册--8-171-基本思想--14h73zm]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 微积分, 几何, 极坐标]
related: [极坐标下的二重积分, 积分应用清单与高维必要性, 圆锥体积由卡瓦列里原理推出]
sources: ["数学指南_实用数学手册/1.7.1 基本思想.md"]
---

# 圆周内部面积由极坐标二重积分算得 πR²

## 论断（例 4）

令 $D$ 为半径 $R$ 的圆围成的区域，则

$$
A = \int_{D}\mathrm{d}x\,\mathrm{d}y = \int_{D'} r\,\mathrm{d}r\,\mathrm{d}\varphi = \int_{0}^{R}\left(\int_{-\pi}^{\pi} r\,\mathrm{d}\varphi\right)\mathrm{d}r = 2\pi\int_{0}^{R} r\,\mathrm{d}r = \pi R^{2}.
$$

## 说明

这是 $\varrho \equiv 1$ 时「二重积分即面积」的直接应用，同时演示了 [[极坐标下的二重积分]] 把圆域上的积分变成两个一维积分的过程。其结果随后被用于例 3 中圆锥 $z$ 截面（圆盘）面积的计算，见 [[圆锥体积由卡瓦列里原理推出]]。

## 相关页面

- [[极坐标下的二重积分]]、[[二重积分]]、[[圆锥体积由卡瓦列里原理推出]]
