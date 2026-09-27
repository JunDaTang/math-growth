---
type: finding
title: 特解 D_par 与 H_par 的性质
source: "[[10-数学指南实用数学手册--23-199-根据源与涡确定向量场向量分析的主要定理--6b4r1d]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [显式解, 散度, 旋度, 位势]
related: [体积位势, 向量位势, 源的规定, 涡流的规定]
sources: ["数学指南_实用数学手册/1.9.9 根据源与涡确定向量场（向量分析的主要定理）.md"]
---

# 特解 D_par 与 H_par 的性质

## 构造

```
D_par := −grad V,   H_par := curl C,
```

其中 $V$ 为 [[体积位势]]，$C$ 为 [[向量位势]]。

## 性质

```
div D_par = ρ,  curl D_par = 0,  在 R^3 上
```

```
div H_par = 0,  curl H_par = J,  在 R^3 上.
```

两条结果互为对偶：$D_{par}$ 只携带源、无旋；$H_{par}$ 只携带涡、无源。因此 $D_{par}$ 与 $H_{par}$ 分别充当 [[源的规定]] 与 [[涡流的规定]] 的显式特解。

## 证据

- 直接证据：来源「解的显式公式」一段的两组公式。

## Related
- [[findings/公式1172同时实现给定散度与旋度]]
