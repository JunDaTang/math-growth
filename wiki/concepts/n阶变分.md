---
type: concept
title: n 阶变分
created: 2026-09-27
updated: 2026-09-27
tags: [数学分析, 多元微积分, 变分, 方向导数]
related: [方向导数, 多元泰勒定理, 变分算子, 偏导数, 高阶偏导数, 弗雷歇导数, 多元链式法则]
sources: ["数学指南_实用数学手册/1.5.8 $n$ 阶变分与泰勒定理.md"]
---
# n 阶变分

**n 阶变分**（$n$-th variation）是《数学指南——实用数学手册》1.5.8 节引入的概念，用于描述多元实值函数沿给定方向的各阶变化率。

## 定义

令 $f: U(\pmb p) \subseteq \mathbb{R}^N \to \mathbb{R}$ 是定义在点 $\pmb p$ 的一个邻域中的函数，$\pmb h \in \mathbb{R}^N$。令

$$
\varphi(t) := f(\pmb p + t\pmb h),
$$

其中实参数 $t$ 在 $t=0$ 的一个小邻域内取值。如果 $n$ 阶导数 $\varphi^{(n)}(0)$ 存在，则数

$$
\delta^{n} f(\boldsymbol{p};\boldsymbol{h}) := \varphi^{(n)}(0)
$$

称为函数 $f$ 在点 $\pmb p$ 处 $\pmb h$ 方向的 $n$ 阶变分。

也就是说，$n$ 阶变分本质上是把函数限制在过点 $\pmb p$、方向 $\pmb h$ 的直线上后所得的**一元函数的 $n$ 阶导数在 $t=0$ 处的取值**。

## 与方向导数的关系

$n=1$ 时得到 [[方向导数]]：$\delta f(\pmb p;\pmb h) := \delta^1 f(\pmb p;\pmb h)$，它等于差商的极限

$$
\delta f(\boldsymbol{p};\boldsymbol{h}) = \lim_{t \to 0} \frac{f(\boldsymbol{p} + t\boldsymbol{h}) - f(\boldsymbol{p})}{t}.
$$

## 用偏导算子幂表示

若 $f$ 在 $\pmb p$ 的开邻域为 $C^n$ 类，则 $n$ 阶变分可用 [[变分算子]] 的幂写出：

$$
\delta^{r} f(\boldsymbol{p};\boldsymbol{h}) = \left(\sum_{k=1}^{N} h_{k} \frac{\partial}{\partial x_{k}}\right)^{r} f(\boldsymbol{p}), \quad r = 1, \dots, n.
$$

该表示把多元高阶变分归约为 [[高阶偏导数]] 的组合，其推导依赖 [[多元链式法则]]，而同类项合并依赖 [[施瓦茨定理]]（混合偏导次序可交换）。

## 与弗雷歇导数的潜在同一性

一阶变分 $\delta f(\pmb p;\pmb h)$ 在 $f$ 可导时即等于 [[弗雷歇导数]]（等价地 [[雅可比矩阵]]）作用于 $\pmb h$ 的结果，但来源并未明说二者等价，故本页只标注潜在同一性，不作硬性合并；辨析见 [[queries/变分与弗雷歇导数是否同一概念]]。

## 相关页面

- [[方向导数]]、[[变分算子]]、[[多元泰勒定理]]、[[高阶偏导数]]、[[偏导数]]