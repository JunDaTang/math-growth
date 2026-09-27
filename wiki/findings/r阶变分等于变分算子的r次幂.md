---
type: finding
title: r 阶变分等于变分算子的 r 次幂
created: 2026-09-27
updated: 2026-09-27
tags: [数学分析, 多元微积分, 变分, 微分算子]
related: [n阶变分, 变分算子, 高阶偏导数, 施瓦茨定理]
sources: ["数学指南_实用数学手册/1.5.8 $n$ 阶变分与泰勒定理.md"]
source: "10-数学指南实用数学手册--14-158-n-阶变分与泰勒定理--13gzzwv"
confidence: high
replicated: null
---
# r 阶变分等于变分算子的 r 次幂

## 结果

在同一 $C^n$ 类前提下，$r$ 阶 [[n阶变分]] 可用 [[变分算子]] 的 $r$ 次幂表示：

$$
\delta^{r} f(\boldsymbol{p};\boldsymbol{h}) = \left(\sum_{k=1}^{N} h_{k} \frac{\partial}{\partial x_{k}}\right)^{r} f(\boldsymbol{p}), \quad r = 1, \dots, n.
$$

## 条件与范围

- 前提：$f$ 在 $\pmb p$ 的开邻域为 $C^n$ 类。
- 该式把高阶变分化为 [[高阶偏导数]] 的有限组合；展开后同类项合并依赖 [[施瓦茨定理]]（混合偏导次序可交换）。

## 证据类型与强度

标准定理，来源直接陈述。置信度高。

## 相关页面

- [[n阶变分]]、[[变分算子]]、[[高阶偏导数]]、[[施瓦茨定理]]

## Related
- [[findings/二元变分算子的平方展开]]
- [[findings/Cn类函数的一阶变分等于偏导加权和]]
