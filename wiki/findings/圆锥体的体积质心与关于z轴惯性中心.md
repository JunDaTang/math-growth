---
type: finding
title: 圆锥体的体积、质心与关于 z 轴惯性中心
created: 2026-09-27
updated: 2026-09-27
tags: [圆锥体, 卡瓦列里原理, 体积, 质心, 惯性中心]
related: [表13曲线坐标下的积分量, 卡瓦列里原理-富比尼定理, 圆柱体的体积质心与关于z轴惯性中心]
sources: ["数学指南_实用数学手册/1.7.10 应用到质心和惯性中点.md"]
source: "[[10-数学指南实用数学手册--15-1710-应用到质心和惯性中点--1eo3sz7]]"
confidence: high
replicated: null
---

# 圆锥体的体积、质心与关于 z 轴惯性中心

## 结论

对以半径为 $R$ 的圆做底、高为 $h$ 的圆锥体（原文例 3，图 1.79(c)）：

- 体积 $M = \dfrac{1}{3}\pi R^{2} h$；
- 质心：$z_{\mathrm{cm}} = \dfrac{h}{4}$（原文此处用词为「质点」），$x_{\mathrm{cm}} = y_{\mathrm{cm}} = 0$；
- 关于 $z$ 轴的惯性中心 $\Theta_z = \dfrac{3}{10} M R^{2}$。

## 推导路径

体积由 [[卡瓦列里原理-富比尼定理]] 按 $z$ 截面计算：

$$
M = \int_{z=0}^{h} \left(\int_{D_z} \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\right)
= \int_{0}^{h} \pi R_z^{2}\,\mathrm{d}z
= \frac{1}{3}\pi R^{2} h,
$$

其中截面半径（引自 1.7.1 中的例 3）为

$$
R_z = \frac{(h - z)R}{h}.
$$

质心：

$$
z_{\mathrm{cm}} = \frac{1}{M}\int_{z=0}^{h}\left(\int_{D_z} z\,\mathrm{d}x\,\mathrm{d}y\right)\mathrm{d}z
= \frac{1}{M}\int_{0}^{h} z \pi R_z^{2}\,\mathrm{d}z
= \frac{h}{4},\qquad x_{\mathrm{cm}} = y_{\mathrm{cm}} = 0 .
$$

惯性中心：

$$
\Theta_z = \int (x^{2}+y^{2})\,\mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z
= \int_{0}^{h}\left(\int_{D_z} r^{3}\,\mathrm{d}r\,\mathrm{d}\varphi\right)\mathrm{d}z
= \int_{0}^{h} \frac{\pi}{2} R_z^{4}\,\mathrm{d}z
= \frac{3}{10} M R^{2}.
$$

## 注意

- 原文质心一处写作「质点」，疑为「质心」的转写讹误，见 [[queries/1710节例3中质点一词是否应为质心]]。
- 所用 $z$ 截面记号 $D_z$ 与 [[z截面]] 一致，体积计算方式与 [[卡瓦列里原理由富比尼定理经平凡扩张推出]]、[[圆锥体积由卡瓦列里原理推出]] 同源。

## 证据类型

直接证据：原文给出完整积分式与结果；$R_z$ 的线性表达式引自动因 1.7.1 节例 3。