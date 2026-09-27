---
type: concept
title: 发散量算子 Div
created: 2026-09-27
updated: 2026-09-27
tags: [算子, 张量代数, 闵可夫斯基几何]
related: [闵可夫斯基空间M4, 霍奇δ算子, Alt算子, 霍奇星算子]
sources: ["数学指南_实用数学手册/3.9.4 闵可夫斯基几何.md"]
---

# 发散量算子 Div

《数学指南》3.9.4 节对 $M_4$ 上的张量场 $F=T^{jk}e_j\otimes e_k$ 定义发散量算子

$$
\boxed {\operatorname{Div} F := \partial_ {j} T ^ {j k} e _ {k},}
$$

其中对既出现在上面也出现在下面的指标从 1 到 4 求和（**爱因斯坦约定**）。

## 说明

- 记号 $\partial_j=\partial/\partial x_j$。
- 正文强调：该公式是一般张量计算公式的特殊情形（可在文献 [212] 中找到），且 $\operatorname{Div}$ 具有不变性意义，不依赖于用来定义它的伪法正交基的选取。
- 在张量代数框架下，$\operatorname{Div}$ 把二阶张量场 $T^{jk}e_j\otimes e_k$ 映射回向量场。

## 关联

- 与 [[霍奇δ算子]]、外导数 $\mathrm d$ 同属本节强调「不依赖伪法正交基选取」的算子族。
- [[Alt算子]] 一起在 3.9.4 节末尾给出定义。