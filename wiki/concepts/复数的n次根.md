---
type: concept
title: 复数的 n 次根
created: 2026-09-27
updated: 2026-09-27
tags: [复数, 方程, 初等分析]
related: [复数的极坐标表示, 单位根, 欧拉公式, 10-数学指南实用数学手册--7-11-初等分析--1gphwdf]
sources: ["数学指南_实用数学手册/1.1 初等分析.md"]
---

# 复数的 n 次根

1.1.2.4 节：设复数 a = |a| e^{iφ}，其中 −π < φ ≤ π 且 a ≠ 0。**定理**：对于固定的 n = 2, 3, …，圆方程

```latex
x^{n} = a
```

的解为

```latex
x = \sqrt[n]{|a|}\left(\cos\left(\frac{2\pi k + \varphi}{n}\right) + \mathrm{i} \cdot \sin\left(\frac{2\pi k + \varphi}{n}\right)\right), \quad k = 0, 1, \dots, n - 1.
```

也可以把这些数记作 `x = ⁿ√|a| · e^{i(2πk + φ)/n}`，k = 0, …, n − 1；它们称为复数 a 的 **n 个根**。这 n 个根把半径为 ⁿ√|a| 的圆周分成 n 等份。

例：2i = 2e^{iπ/2} 的两个根是

```latex
x = \sqrt{2}\left(\cos\frac{\pi}{4} + \mathrm{i}\cdot\sin\frac{\pi}{4}\right) = 1 + \mathrm{i},
x = \sqrt{2}\left(\cos\left(\pi + \frac{\pi}{4}\right) + \mathrm{i}\cdot\sin\left(\pi + \frac{\pi}{4}\right)\right) = -(1 + \mathrm{i})
```

（图 1.11）。a = 1 的情形给出单位根，见 [[concepts/单位根]]。

来源：[[sources/10-数学指南实用数学手册--7-11-初等分析--1gphwdf]]。

## Related
- [[findings/复数的n个根等分圆周]]
