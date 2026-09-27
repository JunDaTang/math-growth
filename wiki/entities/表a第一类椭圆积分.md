---
type: entity
title: 表 a（第一类椭圆积分）
created: 2026-09-27
updated: 2026-09-27
tags: [数学表, 椭圆积分, 数值表]
related: [第一类椭圆积分, 椭圆积分, 表c完全椭圆积分, 模数与模角, 振幅]
sources: ["数学指南_实用数学手册/0.5.4 椭圆积分.md"]
---

# 表 a（第一类椭圆积分）

源文 0.5.4 节 a) 项下的数值表，标题为「第一类椭圆积分 $F(k,\varphi)$，$k = \sin\alpha$」。表为 10×10 的双栏结构：列头为 $\alpha = 0^\circ, 10^\circ, \ldots, 90^\circ$（前 5 列与后 5 列分两段排版），行头为 $\varphi = 0^\circ, 10^\circ, \ldots, 90^\circ$。

源文未给出表号；本 wiki 按内容命名。完整数据见 [[10-数学指南实用数学手册--8-054-椭圆积分--3chh90]]。

## 特征

- 首行（$\varphi = 0^\circ$）全为 `0.000 0`；
- 末行（$\varphi = 90^\circ$）给出 [[完全椭圆积分]] 的 $K$ 值，例如 $\alpha = 0^\circ$ 为 `1.570 8`、$\alpha = 80^\circ$ 为 `3.153 4`、$\alpha = 90^\circ$ 为 $\infty$；
- 全部数值皆随 $\varphi$ 与 $\alpha$ 单调不减。

## 交叉校核

末行与 [[表c完全椭圆积分]] 的 $K$ 列在 $\alpha = 0^\circ, 10^\circ, \ldots, 80^\circ$ 上逐项一致，见 [[表a与表c在φ等于90度处的交叉一致]]。