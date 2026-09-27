---
type: finding
title: 例 2：链式法则给出 (b^x)' = b^x ln b
source: "[[10-数学指南实用数学手册--8-142-链式法则--1lnjr5z]]"
confidence: high
replicated: null
tags: [数学, 微积分, 链式法则, 指数函数, 算例]
related: [链式法则, 复合函数, 表081重要导数表, 欧拉常数]
created: 2026-09-27
updated: 2026-09-27
sources: ["数学指南_实用数学手册/1.4.2 链式法则.md"]
---

# 例 2：链式法则给出 (b^x)' = b^x ln b

## 结果

《数学指南——实用数学手册》1.4.2 节例 2 令 $b > 0$，对函数 $f(x) := b^{x}$ 得到

```latex
f^{\prime}(x) = b^{x} \ln b, \quad x \in \mathbb{R}
```

## 推导过程（逐字保留）

```latex
f(x) = \mathrm{e}^{x \ln b}, \quad y = \mathrm{e}^{u}, \quad u = x \ln b,
\frac{\mathrm{d} y}{\mathrm{d} u} = \mathrm{e}^{u}, \quad \frac{\mathrm{d} u}{\mathrm{d} x} = \ln b,
f^{\prime}(x) = \frac{\mathrm{d} y}{\mathrm{d} x}
= \frac{\mathrm{d} y}{\mathrm{d} u} \frac{\mathrm{d} u}{\mathrm{d} x}
= \mathrm{e}^{u} \ln b = b^{x} \ln b.
```

## 说明

- 关键的第一步是把 $b^{x}$ 改写为 $\mathrm{e}^{x \ln b}$，从而把底数为常数的指数函数化归为以 $\mathrm{e}$ 为底的指数函数。
- 内函数为 $u = x \ln b$（线性函数），外函数为 $y = \mathrm{e}^{u}$。
- 基本导数 $\dfrac{\mathrm{d} y}{\mathrm{d} u} = \mathrm{e}^{u}$ 与 $\dfrac{\mathrm{d} u}{\mathrm{d} x} = \ln b$ 均标注「由 0.8.1」，即 [[表081重要导数表]]。
- 回代 $u = x \ln b$ 并用 $\mathrm{e}^{x \ln b} = b^{x}$ 得到最终结果。
- 该结果对一切 $x \in \mathbb{R}$ 成立（前提 $b > 0$），属直接证据；原书未给出超出上述步骤的论证。

## 相关

- [[链式法则]]、[[复合函数]]
- 同类算例：[[链式法则例1求导sinx平方]]
- 来源：[[10-数学指南实用数学手册--8-142-链式法则--1lnjr5z]]