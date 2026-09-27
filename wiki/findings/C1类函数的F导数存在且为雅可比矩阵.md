---
type: finding
title: C^1 类函数的 F 导数存在且等于雅可比矩阵
source: "[[10-数学指南实用数学手册--9-152-弗雷歇导数--p4bpd6]]"
confidence: medium
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [多变量微积分, 弗雷歇导数, 雅可比矩阵, 主要定理]
related: [弗雷歇导数, 雅可比矩阵, 雅可比行列式, 多元CK类光滑函数, 偏导数]
sources: ["数学指南_实用数学手册/1.5.2 弗雷歇导数.md"]
---

# C^1 类函数的 F 导数存在且等于雅可比矩阵

## 结论（主要定理）

如果 $f: M \subseteq \mathbb{R}^N \to \mathbb{R}^k$ 在点 $p$ 的一个**邻域**中是 $C^1$ 类的，那么 F 导数 $f'(p)$ 存在，并满足

```latex
f'(p) = (\partial_j f_k(p)),
```

即由 $f$ 的各分量一阶偏导数组成的 [[雅可比矩阵]]：

```latex
\boldsymbol{f}'(p) = \begin{pmatrix}
\partial_1 f_1(\boldsymbol{p}) & \partial_2 f_1(\boldsymbol{p}) & \dots & \partial_N f_1(\boldsymbol{p}) \\
\partial_1 f_2(\boldsymbol{p}) & \partial_2 f_2(\boldsymbol{p}) & \dots & \partial_N f_2(\boldsymbol{p}) \\
\vdots & \vdots & & \vdots \\
\partial_1 f_K(\boldsymbol{p}) & \partial_2 f_K(\boldsymbol{p}) & \dots & \partial_N f_K(\boldsymbol{p})
\end{pmatrix}.
```

当 $N = K$ 时，其行列式即 [[雅可比行列式]]。

## 证据强度

**中等偏保守**：本源对该定理**仅作陈述，未给出证明**。前提「$C^1$ 类」的使用见 [[多元CK类光滑函数]]；构造所用的 $\partial_j f_k$ 见 [[偏导数]]。因此本条的置信度标为 medium，而非 high。

## 直接证据与推断的区分

- 直接证据：本源原文的定理陈述与雅可比矩阵的显式形式。
- 推断：定理的证明思路（由中值定理逐分量估计余项 $r(h)$ 为 $o(|h|)$）本源未给，属推断，未在本源中陈述。

## 意义

该定理把 1.5.1 节的偏导数与 1.5.2 节的弗雷歇导数连接起来，说明在 $C^1$ 条件下，多元可微性的**计算**归结为求雅可比矩阵。