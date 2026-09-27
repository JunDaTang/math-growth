---
type: finding
title: arcosh 具有双值性
source: "[[10-数学指南实用数学手册--10-0213-反双曲函数--80sg7]]"
confidence: high
replicated: null
tags: [数学, 双曲函数, 反函数, 多值性]
related: [反双曲函数, 双曲函数, 反双曲函数的对数表示, 反函数]
sources: ["数学指南_实用数学手册/0.2.13 反双曲函数.md"]
created: 2026-09-27
updated: 2026-09-27
---

# arcosh 具有双值性

## 结论

在《数学指南》0.2.13 的表 0.24 中，方程 $y=\cosh x$（$y\geqslant 1$）的解写成

$$
x=\pm\operatorname{arcosh} y=\pm\ln\left(y+\sqrt{y^{2}-1}\right),
$$

即 $\operatorname{arcosh}$ 呈双值形式，而其余三个反双曲函数 $\operatorname{arsinh}$、$\operatorname{artanh}$、$\operatorname{arcoth}$ 的解都是唯一的。

## 依据

- 原文对 $\operatorname{arsinh}$ 明确写出「有且仅有一个解」，而 $\cosh$ 一行直接用 $\pm$ 号给出两个解，二者的对照即说明 $\cosh$ 在 $\mathbb{R}$ 上非单射。
- 表 0.23 中 $\cosh$ 的图像关于 $y$ 轴对称，其反函数图中 $\operatorname{arcosh}$ 只绘出自 $x=1$ 起始的一支曲线，对应双值中的非负分支。
- 从对数表示看，$\ln\left(y+\sqrt{y^{2}-1}\right)$ 与 $-\ln\left(y+\sqrt{y^{2}-1}\right)$ 互为相反数，与 $\cosh$ 的偶性一致。

## 说明

原文并未给出主值（如规定 $\operatorname{arcosh} x\geqslant 0$）的取舍约定，只保留 $\pm$ 写法。因此对 $\operatorname{arcosh}$ 的每一处引用都需明确取哪一支；本 wiki 的 [[反双曲函数]] 页面按原文保留双值形式。

置信度：高（直接来自原文表 0.24 与对 $\sinh$ 的对照陈述）。复制状态：未知（本节为单一来源，尚未与其他文献或手册版本比对）。