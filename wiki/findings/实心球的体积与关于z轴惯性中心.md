---
type: finding
title: 实心球的体积与关于 z 轴惯性中心
created: 2026-09-27
updated: 2026-09-27
tags: [球面坐标, 体积, 质心, 惯性中心]
related: [表13曲线坐标下的积分量, 球面坐标, 表12曲线坐标, 质心与转动惯量]
sources: ["数学指南_实用数学手册/1.7.10 应用到质心和惯性中点.md"]
source: "[[10-数学指南实用数学手册--15-1710-应用到质心和惯性中点--1eo3sz7]]"
confidence: high
replicated: null
---

# 实心球的体积与关于 z 轴惯性中心

## 结论

对中心在原点、半径为 $R$ 的实心球（原文例 1，图 1.79(a)）：

- 体积 $M = \dfrac{4\pi R^{3}}{3}$；
- 质心位于球的中心，即原点；
- 关于 $z$ 轴的惯性中心 $\Theta_z = \dfrac{2}{5} R^{2} M$。

## 推导路径

在球面坐标下按 [[表13曲线坐标下的积分量]] 立体行计算：

$$
M = \int r^{2}\cos\theta \,\mathrm{d}\theta\,\mathrm{d}\varphi\,\mathrm{d}r
= \int_{0}^{R} r^{2}\mathrm{d}r \int_{-\pi}^{\pi} \mathrm{d}\varphi \int_{-\pi/2}^{\pi/2} \cos\theta \,\mathrm{d}\theta
= \frac{4\pi R^{3}}{3},
$$

$$
\Theta_z = \int (r\cos\theta)^{2} r^{2}\cos\theta \,\mathrm{d}\theta\,\mathrm{d}\varphi\,\mathrm{d}r
= \int_{0}^{R} r^{4}\mathrm{d}r \int_{-\pi}^{\pi} \mathrm{d}\varphi \int_{-\pi/2}^{\pi/2} \cos^{3}\theta \,\mathrm{d}\theta
= \frac{2}{5} R^{2} M .
$$

## 注意

- 卫星体积公式中把体积记为 $M$，是因为表 1.3 在 $\rho = 1$ 时质量即体积；并非把体积与质量混用。
- 本例的角 $\theta$ 取值范围为 $[-\pi/2, \pi/2]$，即从赤道面量起，与本手册球面坐标的约定一致，参见 [[球面坐标]] 与 [[球面坐标θ从赤道量起]]。
- 球面坐标的体积元素形式见 [[表12曲线坐标]]、[[体积形式]]。

## 证据类型

直接证据：原文给出完整积分式与结果。