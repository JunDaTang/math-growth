---
type: finding
title: 圆柱体的体积、质心与关于 z 轴惯性中心
created: 2026-09-27
updated: 2026-09-27
tags: [柱面坐标, 体积, 质心, 惯性中心]
related: [表13曲线坐标下的积分量, 柱面坐标, 表12曲线坐标, 质心与转动惯量]
sources: ["数学指南_实用数学手册/1.7.10 应用到质心和惯性中点.md"]
source: "[[10-数学指南实用数学手册--15-1710-应用到质心和惯性中点--1eo3sz7]]"
confidence: high
replicated: null
---

# 圆柱体的体积、质心与关于 z 轴惯性中心

## 结论

对半径为 $R$、高为 $h$ 的圆柱体（原文例 2，图 1.79(b)）：

- 体积 $M = \pi R^{2} h$；
- 质心：$z_{\mathrm{cm}} = \dfrac{h}{2}$，$x_{\mathrm{cm}} = y_{\mathrm{cm}} = 0$；
- 关于 $z$ 轴的惯性中心 $\Theta_z = \dfrac{1}{2} R^{2} M$。

## 推导路径

在柱面坐标下按 [[表13曲线坐标下的积分量]] 立体行计算：

$$
M = \int r \,\mathrm{d}r\,\mathrm{d}\varphi\,\mathrm{d}z
= \int_{0}^{R} r\,\mathrm{d}r \int_{-\pi}^{\pi} \mathrm{d}\varphi \int_{0}^{h} \mathrm{d}z
= \pi R^{2} h,
$$

$$
\Theta_z = \int r^{2}\cdot r \,\mathrm{d}\varphi\,\mathrm{d}r\,\mathrm{d}z
= \int_{0}^{R} r^{3}\mathrm{d}r \int_{-\pi}^{\pi} \mathrm{d}\varphi \int_{0}^{h} \mathrm{d}z
= \frac{1}{2} R^{2} M .
$$

## 注意

- 柱面坐标的约定与体积元素见 [[柱面坐标]] 与 [[表12曲线坐标]]。
- 质心位于轴线上高度一半处，符合圆柱的对称性。

## 证据类型

直接证据：原文给出完整积分式与结果。