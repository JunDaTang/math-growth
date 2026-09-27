---
type: finding
title: 例：sinh 是 ℝ 上的 C^∞ 类微分同胚
created: 2026-09-27
updated: 2026-09-27
tags: [例子, sinh, 微分同胚, 阿达马定理]
related: [整体微分同胚的阿达马定理, 微分同胚, 阿达马]
sources: ["数学指南_实用数学手册/1.5.7 逆映射.md"]
source: "[[10-数学指南实用数学手册--7-157-逆映射--3o8794]]"
confidence: high
replicated: null
---

# 例：sinh 是 ℝ 上的 C^∞ 类微分同胚

**结论（直接来自源文档）：** 令 $N = 1$，$f(x) := \sinh x$。此时 $f'(x) = \cosh x > 0$，故 $\det f'(x) \neq 0$ 在 $\mathbb{R}$ 上处处成立，蕴涵 (1.79) 成立；配合 $|x| \to \infty$ 时 $|\sinh x| \to +\infty$，得 $f: \mathbb{R} \to \mathbb{R}$ 是 $C^\infty$ 类[[微分同胚]]。

**它是[[整体微分同胚的阿达马定理]]在 $N = 1$ 情形下的唯一具体示例。** 源文档图 1.51 给出相应曲线示意（一条从左下到右上、过原点的单调递增曲线）。

**证据类型：** 直接可验证的初等计算，confidence 高。
