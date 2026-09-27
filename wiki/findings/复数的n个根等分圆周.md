---
type: finding
title: 复数的 n 个根把圆周 n 等分
source: "[[10-数学指南实用数学手册--7-11-初等分析--1gphwdf]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [复数, 方程, 几何, 初等分析]
related: [复数的n次根, 单位根, 复数的极坐标表示, 10-数学指南实用数学手册--7-11-初等分析--1gphwdf]
sources: ["数学指南_实用数学手册/1.1 初等分析.md"]
---

# 复数的 n 个根把圆周 n 等分

## 观察

1.1.2.4 节定理：对固定的 n = 2, 3, …，方程 xⁿ = a（a ≠ 0）的 n 个根为

```latex
x = \sqrt[n]{|a|}\left(\cos\left(\frac{2\pi k + \varphi}{n}\right) + \mathrm{i}\cdot\sin\left(\frac{2\pi k + \varphi}{n}\right)\right), \quad k = 0, 1, \dots, n - 1,
```

它们把半径为 ⁿ√|a| 的圆周分成 n 等份。

## 证据

- a = 1 时给出单位根（图 1.10，n = 2, 3, 4）。
- a = 2i = 2e^{iπ/2} 时两个根为 x = 1 + i 与 x = −(1 + i)，互为对原点对称（图 1.11）。
- 手册另行给出等价记号 `x = ⁿ√|a| e^{i(2πk + φ)/n}`。

## 评估

结论取自复数的极坐标表示与欧拉公式，属教科书级定理；手册以几何语言（等分圆周）陈述其意义。

相关页面：[[concepts/复数的n次根]]、[[concepts/单位根]]。来源：[[sources/10-数学指南实用数学手册--7-11-初等分析--1gphwdf]]。

## Related
- [[findings/欧拉公式建立指数与三角函数的关系]]
