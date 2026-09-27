---
type: finding
title: lcm 与 gcd 的素数分解求法及例 5、例 6
source: "[[10-数学指南实用数学手册--10-272-欧几里得算法--8lmmzy]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [数论, lcm, gcd, 素因数分解]
related: [最小公倍数与最大公约数, 算术基本定理, 欧几里得算法, 素数]
sources: ["数学指南_实用数学手册/2.7.2 欧几里得算法.md"]
---

# lcm 与 gcd 的素数分解求法及例 5、例 6

## 观察

对正自然数 $m$、$n$：

- **最小公倍数** $\operatorname{lcm}(m, n)$：把 $m$、$n$ 素数分解式中所有素因子相乘（共同出现的每个只取一次）。
- **最大公约数** $\operatorname{gcd}(m, n)$：把同时出现在 $m$、$n$ 分解式中的素数相乘。

## 证据

沿用例 4 的 $24 = 2 \cdot 2 \cdot 2 \cdot 3$ 与 $28 = 2 \cdot 2 \cdot 7$：

- 例 5：$\operatorname{lcm}(24, 28) = 2 \cdot 2 \cdot 2 \cdot 3 \cdot 7 = 168$。
- 例 6：$\gcd(24, 28) = 2 \cdot 2 = 4$。

## 说明

源中随后给出的[[欧几里得算法]]提供了求 $\gcd$ 的另一条（不依赖分解的）路径；两条路径在本小节内并列呈现。

## 相关页面

- [[最小公倍数与最大公约数]]
- [[算术基本定理]]
- [[欧几里得算法]]
