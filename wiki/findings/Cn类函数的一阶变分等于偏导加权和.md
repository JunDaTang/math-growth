---
type: finding
title: C^n 类函数的一阶变分等于偏导加权和
created: 2026-09-27
updated: 2026-09-27
tags: [数学分析, 多元微积分, 变分, 偏导数]
related: [n阶变分, 方向导数, 偏导数, 局部Ck类]
sources: ["数学指南_实用数学手册/1.5.8 $n$ 阶变分与泰勒定理.md"]
source: "10-数学指南实用数学手册--14-158-n-阶变分与泰勒定理--13gzzwv"
confidence: high
replicated: null
---
# C^n 类函数的一阶变分等于偏导加权和

## 结果

令 $n \geqslant 1$。如果 $f: U(\pmb p) \subseteq \mathbb{R}^N \to \mathbb{R}$ 是在点 $\pmb p$ 的一个开邻域的 $C^n$ 类函数，则一阶 [[n阶变分]]（即 [[方向导数]]）等于各 [[偏导数]] 以方向分量为权的线性组合：

$$
\delta f(\boldsymbol{p};\boldsymbol{h}) = \sum_{k=1}^{N} h_{k} \frac{\partial f(\boldsymbol{p})}{\partial x_{k}}.
$$

## 条件与范围

- 前提：$f$ 在 $\pmb p$ 的**开邻域**为 $C^n$ 类（对比 [[多元泰勒定理]] 所用的开凸集前提）。
- 结论把方向导数归约为梯度（[[雅可比矩阵]] 行向量）与方向的内积。

## 证据类型与强度

标准定理，来源直接陈述。置信度高。未给出证明。

## 相关页面

- [[n阶变分]]、[[方向导数]]、[[偏导数]]、[[局部Ck类]]

## Related
- [[findings/多元泰勒定理要求开凸集与Cn加1类]]
- [[findings/变分定义为沿直线的n阶导数]]
