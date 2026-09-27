---
type: finding
title: 极坐标自然基向量中 er 为单位向量、eφ 长度为 r
source: "[[10-数学指南实用数学手册--8-179-曲线坐标--1aid11y]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 极坐标, 自然基, 曲线坐标]
related: [极坐标, 自然基向量与自然分量, 曲线坐标]
sources: ["数学指南_实用数学手册/1.7.9 曲线坐标.md"]
---

# 极坐标自然基向量中 er 为单位向量、eφ 长度为 r

## 结论

在极坐标变换 $x = r\cos\varphi,\ y = r\sin\varphi$（$-\pi<\varphi\le\pi,\ r\ge0$）下，点 $P$ 处的自然基向量为

$$
\boldsymbol e_r = \boldsymbol r_r = \cos\varphi\,\boldsymbol i + \sin\varphi\,\boldsymbol j,
$$

$$
\boldsymbol e_\varphi = \boldsymbol r_\varphi = -r\sin\varphi\,\boldsymbol i + r\cos\varphi\,\boldsymbol j.
$$

$\boldsymbol e_r$ 的模为 $1$，而 $\boldsymbol e_\varphi$ 的模为 $r$。

## 依据

由分量直接计算：$|\boldsymbol e_r| = \sqrt{\cos^2\varphi + \sin^2\varphi} = 1$；$|\boldsymbol e_\varphi| = \sqrt{r^2\sin^2\varphi + r^2\cos^2\varphi} = r$。二者内积为零，故正交。

## 意义

该事实说明本节采用的是**坐标切向量基（自然基）** 而非归一化单位基。$\boldsymbol e_\varphi$ 的长度 $r$ 正好解释了极坐标面积元中出现的因子 $r$（见 [[极坐标面积元为r dr dphi]]），也是[[度量张量]]对角分量 $g_{\varphi\varphi} = r^2$ 的来源。

## Related
- [[findings/柱面坐标三条坐标线两两垂直且过每点唯一]]
