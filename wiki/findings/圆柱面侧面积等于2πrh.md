---
type: finding
title: 半径 r 高 h 的圆柱面侧面积等于 2πrh
source: "[[10-数学指南实用数学手册--8-179-曲线坐标--1aid11y]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 柱面坐标, 面积, 曲面积分]
related: [柱面坐标, 曲面面积元, 柱面坐标弧长元素与体积形式]
sources: ["数学指南_实用数学手册/1.7.9 曲线坐标.md"]
---

# 半径 r 高 h 的圆柱面侧面积等于 2πrh

## 结论

对 $r = $ 常数的圆柱面，体积形式退化为 $\mu = r\,\mathrm d\varphi \wedge \mathrm dz$，面积积分为

$$
\int \varrho\,\mathrm dF = \int \varrho\,\mu = \int \varrho\, r\,\mathrm d\varphi\,\mathrm dz.
$$

取 $\varrho \equiv 1$，半径为 $r$、高为 $h$ 的圆柱面（不含上、下底）的面积为

$$
\int_{z=0}^{h}\left(\int_{\varphi=-\pi}^{\pi} r\,\mathrm d\varphi\right)\mathrm dz = 2\pi r h.
$$

## 依据

内层积分 $\int_{-\pi}^{\pi} r\,\mathrm d\varphi = 2\pi r$ 给出周长，再对 $z$ 从 $0$ 到 $h$ 积分即得侧面积。原文明确注明该面积为**曲面面积，不含上、下底**。

## 备注

原文内层积分的上下限写作 $\varphi$ 从 $-\pi$ 到 $\pi$，与坐标变换中 $\varphi$ 的半开区间 $(-\pi,\pi]$ 在端点选取上略有差别，但对积分值无影响。