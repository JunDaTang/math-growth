---
type: finding
title: 单位圆反演 w = 1/z 的几何构造
created: 2026-09-27
updated: 2026-09-27
tags: [复变函数, 共形映射, 反演]
related: [单位圆上的反演, 共形映射, 双全纯映射, 默比乌斯变换]
sources: ["数学指南_实用数学手册/1.14.11 共形映射的例子.md"]
source: "10-数学指南实用数学手册--13-11411-共形映射的例子--18583k5"
confidence: high
replicated: null
---

# 单位圆反演 w = 1/z 的几何构造

## 内容

映射

$$
w = \frac{1}{z} \quad \text{对所有满足 } z \neq 0 \text{ 的 } z \in \mathbb{C}
$$

是双全纯的，因而是从有孔复平面 $\mathbb{C} - \{0\}$ 到自身的 [[共形映射]]。

令 $z = r\mathrm{e}^{\mathrm{i}\varphi}$，则

$$
w = \frac{1}{r}\mathrm{e}^{-\mathrm{i}\varphi}.
$$

由于 $|w| = 1/|z|$，点 $w$ 的构造方式是：先取点 $z$ 关于单位圆周的反演点，再关于实轴作反射（源文档图 1.181）。

## 意义

该映射是 [[单位圆上的反演]] 这一概念的来源，也是 [[默比乌斯变换]] 的四类生成元之一（反演部分）。它解释了为什么 $\operatorname{Aut}(\overline{\mathbb{C}})$ 必须把直线并入 [[广义圆]]：反演会把过原点的圆变为直线。

## 出处

《数学指南——实用数学手册》1.14.11.2。