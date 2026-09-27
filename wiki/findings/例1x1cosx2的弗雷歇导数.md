---
type: finding
title: 例 1：f(x) = x₁cos x₂ 在 (0,0) 处的弗雷歇导数为 (1,0)
source: "[[10-数学指南实用数学手册--9-152-弗雷歇导数--p4bpd6]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [多变量微积分, 弗雷歇导数, 例题, 线性近似]
related: [弗雷歇导数, 雅可比矩阵, 线性化与线性近似, 偏导数]
sources: ["数学指南_实用数学手册/1.5.2 弗雷歇导数.md"]
---

# 例 1：f(x) = x₁cos x₂ 在 (0,0) 处的弗雷歇导数为 (1,0)

## 例题设定

$K = 1$ 的情形：对 $N$ 个实变量的实值函数 $f: M \subseteq \mathbb{R}^N \to \mathbb{R}$，有

```latex
\boldsymbol{f}'(\boldsymbol{p}) = \left(\partial_1 \boldsymbol{f}(\boldsymbol{p}), \dots, \partial_N \boldsymbol{f}(\boldsymbol{p})\right).
```

取 $f(\boldsymbol{x}) := x_1 \cos x_2$，则

```latex
\partial_1 f(\boldsymbol{x}) = \cos x_2, \quad \partial_2 f(\boldsymbol{x}) = -x_1 \sin x_2,
```

因此

```latex
\boldsymbol{f}'(0, 0) = \left(\partial_1 f(0, 0), \partial_2 f(0, 0)\right) = (1, 0).
```

## 线性化验证

本源用泰勒展开式

```latex
\cos h_2 = 1 - \frac{(h_2)^2}{2} + \dots
```

对 $\boldsymbol{p} = (0,0)^{\mathrm{T}}$、$\boldsymbol{h} = (h_1, h_2)^{\mathrm{T}}$ 及很小的 $h_1, h_2$，得到

```latex
f(\boldsymbol{p} + \boldsymbol{h}) - f(\boldsymbol{p}) = f'(\boldsymbol{p})\boldsymbol{h} + r(\boldsymbol{h}) = (1, 0) \binom{h_1}{h_2} + r(\boldsymbol{h}),
```

其中 $r$ 表示高阶的项。结论：$f'(p)h = h_1$ 可以看成 $f(h) = h_1\cos h_2$ 的线性近似，当 $h_1, h_2$ 足够小。

## 证据与备注

- 证据强度：**高**（逐项求偏导 + 泰勒展开直接验证）。
- 转写疑点：本源此处的中间式子写作 $f(\boldsymbol{p}+\boldsymbol{h}) - f(\boldsymbol{h}) = h_1 + r(\boldsymbol{h})$，按上下文应为 $f(\boldsymbol{p}+\boldsymbol{h}) - f(\boldsymbol{p})$，见 [[152节公式转写疑误汇总]]。

## 相关

本例题是 [[线性化与线性近似]] 与 [[可导意味着线性化]] 的具体示范；其导数值由 [[雅可比矩阵]]（此处退化为行向量）给出。

## Related
- [[findings/C1类函数的F导数存在且为雅可比矩阵]]
