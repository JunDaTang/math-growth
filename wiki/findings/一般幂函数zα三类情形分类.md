---
type: finding
title: 一般幂函数 z^α 的三类情形
source: "[[10-数学指南实用数学手册--15-11415-解析延拓与恒等原理--1d5agap]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [复分析, 幂函数, 多值函数, 解析延拓]
related: [一般幂函数, 黎曼面, 对数主值, 分支点, 例6对数主值绕m圈得加2πmi]
sources: ["数学指南_实用数学手册/1.14.15 解析延拓与恒等原理.md"]
---

# 一般幂函数 z^α 的三类情形

## 源文陈述

一般幂函数：令 $\alpha \in \mathbb{C}$，则对满足 $z > 0$ 所有的 $z \in \mathbb{R}$，有

```text
z^α = e^{α ln z}
```

等号右边的函数可以解析延拓。此解析延拓为函数 $w = z^{\alpha}$。

- (i) 如果 $\operatorname{Re}\alpha$ 与 $\operatorname{Im}\alpha$ 是整数，则 $w = z^{\alpha}$ 在 $\mathbb{C}$ 上是唯一定义。
- (ii) 如果 $\operatorname{Re}\alpha$ 与 $\operatorname{Im}\alpha$ 是有理数而不是整数，则 $w = z^{\alpha}$ 有有限个值（有如对辐角有限多个值的那么多个值）。
- (iii) 如果 $\operatorname{Re}\alpha$ 与 $\operatorname{Im}\alpha$ 是无理数，则 $w = z^{\alpha}$ 有无穷多个值。

在情形 (ii)，$w = z^{\alpha}$ 的直观黎曼面与函数 $w = \sqrt[n]{z}$ 的一样，其中 $n \geqslant 2$ 为某一自然数。

在情形 (iii)，$w = z^{\alpha}$ 的直观黎曼面与函数 $w = \mathrm{Ln}\, z$ 的一样。

## 分类要点

| 情形 | 条件 | 取值个数 | 黎曼面形态 |
|---|---|---|---|
| (i) | $\operatorname{Re}\alpha, \operatorname{Im}\alpha$ 为整数 | 单值 | 定义于 $\mathbb{C}$ |
| (ii) | 有理数而非整数 | 有限多个 | 同 $\sqrt[n]{z}$（$n \geqslant 2$） |
| (iii) | 无理数 | 无穷多个 | 同 $\mathrm{Ln}\, z$ |

## 相关页面

- [[一般幂函数]]、[[黎曼面]]、[[对数主值]]、[[分支点]]
- [[例6对数主值绕m圈得加2πmi]]：情形 (iii) 的延拓机制。