---
type: finding
title: 例 1：链式法则给出 f'(x) = 2x cos x²
source: "[[10-数学指南实用数学手册--8-142-链式法则--1lnjr5z]]"
confidence: high
replicated: null
tags: [数学, 微积分, 链式法则, 算例]
related: [链式法则, 复合函数, 莱布尼茨符号, 表081重要导数表]
created: 2026-09-27
updated: 2026-09-27
sources: ["数学指南_实用数学手册/1.4.2 链式法则.md"]
---

# 例 1：链式法则给出 f'(x) = 2x cos x²

## 结果

《数学指南——实用数学手册》1.4.2 节例 1 对 $y = f(x) = \sin x^{2}$ 求导，结果为

```latex
f^{\prime}(x) = 2x \cos x^{2}
```

## 推导过程（逐字保留）

```latex
y = \sin u, \quad u = x^{2},
\frac{\mathrm{d} y}{\mathrm{d} u} = \cos u, \quad \frac{\mathrm{d} u}{\mathrm{d} x} = 2x,
f^{\prime}(x) = \frac{\mathrm{d} y}{\mathrm{d} x}
= \frac{\mathrm{d} y}{\mathrm{d} u} \frac{\mathrm{d} u}{\mathrm{d} x}
= 2x \cos u = 2x \cos x^{2}.
```

## 说明

- 内函数为 $u = x^{2}$，外函数为 $y = \sin u$，符合 [[复合函数]] 的拆分模式。
- 两个基本导数 $\dfrac{\mathrm{d} y}{\mathrm{d} u} = \cos u$ 与 $\dfrac{\mathrm{d} u}{\mathrm{d} x} = 2x$ 均标注「根据 0.8.1」，即 [[表081重要导数表]]。
- 结果中须把 $u$ 回代为 $x^{2}$，最终为 $2x \cos x^{2}$。
- 本结果为直接计算，属直接证据；原书未附证明，也未给出中间步骤之外的额外论证。

## 相关

- [[链式法则]]、[[莱布尼茨符号]]
- 同类算例：[[链式法则例2给出b的x次幂的导数]]
- 来源：[[10-数学指南实用数学手册--8-142-链式法则--1lnjr5z]]