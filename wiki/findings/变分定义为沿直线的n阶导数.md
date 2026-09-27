---
type: finding
title: 变分定义为沿直线的 n 阶导数
created: 2026-09-27
updated: 2026-09-27
tags: [数学分析, 多元微积分, 变分]
related: [n阶变分, 方向导数]
sources: ["数学指南_实用数学手册/1.5.8 $n$ 阶变分与泰勒定理.md"]
source: "10-数学指南实用数学手册--14-158-n-阶变分与泰勒定理--13gzzwv"
confidence: high
replicated: null
---
# 变分定义为沿直线的 n 阶导数

## 结果

在《数学指南——实用数学手册》1.5.8 节中，$n$ 阶 [[n阶变分]] 被直接定义为把函数限制于过点 $\pmb p$、方向 $\pmb h$ 的直线之后所得一元函数的 $n$ 阶导数在 $t=0$ 处的取值：

$$
\delta^{n} f(\boldsymbol{p};\boldsymbol{h}) := \varphi^{(n)}(0), \quad \varphi(t) := f(\pmb p + t\pmb h).
$$

## 条件与范围

- 对象：$f: U(\pmb p) \subseteq \mathbb{R}^N \to \mathbb{R}$。
- 前提：$\varphi^{(n)}(0)$ 存在。
- $n=1$ 时退化为 [[方向导数]] 的差商极限形式。

## 证据类型与强度

定义性陈述，直接引自来源。置信度高。该定义为后续用偏导算子幂表示变分的定理提供了出发点。

## 相关页面

- [[n阶变分]]、[[方向导数]]