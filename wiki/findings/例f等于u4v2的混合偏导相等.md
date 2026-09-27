---
type: finding
title: 例 1：f(u,v) = u⁴v² 的各阶偏导数
tags: [数学, 分析学, 多元函数, 算例]
source: "[[10-数学指南实用数学手册--7-151-偏导数--1jv1z0r]]"
confidence: high
replicated: null
sources: ["数学指南_实用数学手册/1.5.1 偏导数.md"]
related: [偏导数, 高阶偏导数, 施瓦茨定理]
created: 2026-09-27
updated: 2026-09-27
---

# 例 1：f(u,v) = u⁴v² 的各阶偏导数

## 结果

对于 $f(u,v) = u^4v^2$，来源给出：

```text
f_u  = 4u^3 v^2
f_v  = 2u^4 v
f_uv = f_vu = 8u^3 v
f_uu = 12u^2 v^2
f_uuv = f_uvu = 24u^2 v
```

## 说明

该例展示了：

1. 一阶偏导 $f_u$、$f_v$ 的求法；
2. 混合偏导数相等 $f_{uv} = f_{vu}$；
3. 二阶纯偏导 $f_{uu}$；
4. 三阶混合偏导数相等 $f_{uuv} = f_{uvu}$——即施瓦茨定理推广部分（直到 $k$ 阶的偏导数与先后次序无关）在该函数上的体现。

## 证据性质

来源中的直接算例，属于直接证据。

## Related
- [[findings/例函数u方v立方的偏导数与混合偏导]]
