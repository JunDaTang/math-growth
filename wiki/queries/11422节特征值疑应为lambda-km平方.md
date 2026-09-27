---
type: query
title: "1.14.22 节特征值写作 λ = λ_km 是否应为 λ = λ_km²？"
created: 2026-09-27
updated: 2026-09-27
tags: [记号疑误, 特征值问题]
related: [单位圆盘上的狄利克雷特征值问题, 贝塞尔函数, 薄膜振动的初边值问题]
sources: ["数学指南_实用数学手册/1.14.22 在贝塞尔微分方程上的应用.md"]
---

# 1.14.22 节特征值写作 λ = λ_km 是否应为 λ = λ_km²？

## 问题

来源《数学指南——实用数学手册》1.14.22 在特征值问题 (1.500)

$$-v_{xx} - v_{yy} = \lambda v \quad (D), \qquad v = 0 \quad (\partial D)$$

中给出特征解

$$v_{km}(x, y) = \frac{1}{\sqrt{\pi}\,|J_k'(\lambda_{km})|} J_k(\lambda_{km} r)\, \mathrm{e}^{\mathrm{i}k\varphi}, \qquad \lambda = \lambda_{km},$$

同时定义 $\lambda_{k1} < \lambda_{k2} < \cdots$ 为 $J_k$ 的零点。

## 疑点

- 把 $v_{km}$ 的径向因子写成 $J_k(\lambda_{km} r)$ 时，由贝塞尔方程可得 $-v_{xx} - v_{yy} = \lambda_{km}^2 v$，即拉普拉斯算子在该模式上对应的特征值应为 $\lambda_{km}^2$。
- 若按原文取 $\lambda = \lambda_{km}$，则 $v = J_k(\lambda_{km} r)\mathrm{e}^{\mathrm{i}k\varphi}$ 代入 (1.500) 后得不到 $\lambda v$（相差一个平方）。
- 另一处旁证：[[薄膜振动的初边值问题]] 的解中时间因子为 $\cos(\lambda_{km} t)$、$\sin(\lambda_{km} t)$，其频率为 $\lambda_{km}$，而波动方程的频率等于特征值的平方根——这与 (1.500) 中特征值为 $\lambda_{km}^2$ 相容。

## 影响

- 若确为笔误，则 (1.500) 的「特征值」应记作 $\lambda = \lambda_{km}^2$，而 $\lambda_{km}$ 是频率/零点。
- 需要核对同书其它使用同一特征值问题的小节（如 1.13.2.13）以确认惯例。