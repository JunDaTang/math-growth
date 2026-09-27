---
type: finding
title: 例：F(u,v)=uv^2 的链式法则验证得 4x^3
confidence: high
replicated: null
source: "[[10-数学指南实用数学手册--8-153-链式法则--1rvcoyb]]"
tags: [数学, 链式法则, 例题, 偏导数]
related: [多元链式法则, 偏导数, 复合函数]
created: 2026-09-27
updated: 2026-09-27
sources: ["数学指南_实用数学手册/1.5.3 链式法则.md"]
---

# 例：F(u,v)=uv^2 的链式法则验证得 4x³

## 设定

令 $F(u, v) := uv^2$，而 $u = x^2$、$v = x$，于是

$$
F(x) := F(u(x), v(x)) = x^4. \tag{1.54}
$$

## 计算

按 (1.52)（启发式链式法则）：

$$
\frac{\partial F}{\partial x}
= F_u\frac{\partial u}{\partial x} + F_v\frac{\partial v}{\partial x}
= v^2(2x) + 2uv
= 4x^3.
$$

核对：$v^2 = x^2$，$u = x^2$，$v = x$，故 $v^2(2x) = 2x^3$，$2uv = 2x^3$，和为 $4x^3$。

## 与直接求导的一致性

由 (1.54) 直接求导有 $F'(x) = 4x^3$，与链式法则结果相同。源文以此为例说明链式法则的形式运算给出正确结果。

## 证据强度

强。这是可逐步核验的具体数值例子。注意其在记号上的特殊性：这里 $u, v$ 只依赖单一变量 $x$，源文仍使用了偏导号 $\partial$ 而非 (1.52) 的常导号 $\mathrm{d}$，见 [[queries/153节公式转写疑误汇总]]。
