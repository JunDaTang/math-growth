---
type: finding
title: 例：f(x) = e^{ix} 的导数为 i e^{ix}
source: "[[10-数学指南实用数学手册--8-146-复值函数--1peybqo]]"
confidence: high
replicated: false
tags: [数学, 复分析, 微分法, 例子, 欧拉公式]
related: [复值函数, 复值函数可导的实虚判据, 欧拉公式, 10-数学指南实用数学手册--8-146-复值函数--1peybqo]
sources: ["数学指南_实用数学手册/1.4.6 复值函数.md"]
created: 2026-09-27
updated: 2026-09-27
---

# 例：$f(x)=\mathrm{e}^{\mathrm{i}x}$ 的导数为 $\mathrm{i}\mathrm{e}^{\mathrm{i}x}$

## 陈述

对于 $f(x) := \mathrm{e}^{\mathrm{i}x}$，有

$$
f^{\prime}(x)=\mathrm{i}\mathrm{e}^{\mathrm{i}x}, \quad x \in \mathbb{R}.
$$

## 原文证明

由欧拉公式 $f(x)=\cos x+\mathrm{i}\sin x$ 及 (1.40) 即得：

$$
f'(x)=-\sin x+\mathrm{i}\cos x=\mathrm{i}(\cos x+\mathrm{i}\sin x). \quad \square
$$

## 证明的依赖结构

该证明同时依赖两件事：

1. [[欧拉公式]]，把 $\mathrm{e}^{\mathrm{i}x}$ 改写为 $\cos x + \mathrm{i}\sin x$；
2. 复用 [[复值函数可导的实虚判据|实虚判据 (1.40)]]，把复值函数的求导拆成实部与虚部两个实值函数的求导。

其中 (1.40) 在本节中是先被陈述、随后被本例引用的定理，本节未对其另行证明。此外，证明隐含使用了 $(\sin x)' = \cos x$ 与 $(\cos x)' = -\sin x$ 这两个实值导数结果（参见表 0.8.1 重要导数表）。

## 意义

该例是 [[欧拉公式]] 与 1.4 节微分法交汇的示范：它同时说明复指数函数的导数仍是自身的常数倍，且比例常数为 $\mathrm{i}$。