---
type: finding
title: 例：f(u,v) = u²v³ 的偏导数与混合偏导
tags: [数学, 分析学, 多元函数, 算例]
source: "[[10-数学指南实用数学手册--7-151-偏导数--1jv1z0r]]"
confidence: high
replicated: null
sources: ["数学指南_实用数学手册/1.5.1 偏导数.md"]
related: [偏导数, 高阶偏导数, 施瓦茨定理]
created: 2026-09-27
updated: 2026-09-27
---

# 例：f(u,v) = u²v³ 的偏导数与混合偏导

## 结果

对 $f(u,v) := u^2v^3$：

```text
(1.42)  ∂f/∂u = 2uv^3
(1.43)  ∂f/∂v = 3u^2v^2
∂²f/∂v∂u = ∂/∂v(∂f/∂u) = 6uv^2
∂²f/∂u∂v = ∂/∂u(∂f/∂v) = 6uv^2
```

## 说明

该例同时演示了两件事：一阶偏导数的计算方式；以及两个混合偏导数 $\partial^2 f/\partial v\partial u$ 与 $\partial^2 f/\partial u\partial v$ 在此例中取值相同（均等于 $6uv^2$）。来源借此引出对足够光滑函数成立的对称性 $f_{uv} = f_{vu}$，并指向 [[施瓦茨定理]] (1.44)。

## 证据性质

来源中的直接算例，属于直接证据。

## Related
- [[findings/施瓦茨定理推广至k阶偏导次序无关]]
- [[findings/偏导数把其他变量视为常数]]
- [[findings/例f等于u4v2的混合偏导相等]]
