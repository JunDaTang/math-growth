---
type: finding
title: 定理 2：GL(2,C) → Aut(C̄) 的群同态与 PGL(2,C) 同构
created: 2026-09-27
updated: 2026-09-27
tags: [代数, 群同态, 默比乌斯变换, 射影群]
related: [复射影群, 复平面自同构群, 默比乌斯变换]
sources: ["数学指南_实用数学手册/1.14.11 共形映射的例子.md"]
source: "10-数学指南实用数学手册--13-11411-共形映射的例子--18583k5"
confidence: high
replicated: null
---

# 定理 2：GL(2,C) → Aut(C̄) 的群同态与 PGL(2,C) 同构

## 内容

令 $GL(2, \mathbb{C})$ 为所有 $2 \times 2$ 复可逆矩阵构成的群；令 $D$ 为其中所有形如 $\lambda I$（$\lambda \neq 0$）的矩阵构成的子群，$I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$。

**定理 2**：映射

$$
\begin{pmatrix} a & b \\ c & d \end{pmatrix} \mapsto \frac{az + b}{cz + d}
$$

是从 $GL(2, \mathbb{C})$ 到 $\operatorname{Aut}(\overline{\mathbb{C}})$ 的群同态，其**核为 $D$**。因而存在群同构

$$
GL(2, \mathbb{C}) / D \cong \operatorname{Aut}(\overline{\mathbb{C}}),
$$

即 $\operatorname{Aut}(\overline{\mathbb{C}})$ 同构于复射影群 $PGL(2, \mathbb{C})$。

## 意义

该定理说明：[[默比乌斯变换]] 与 $2 \times 2$ 复矩阵在标量倍数意义下一一对应，因而 [[复平面自同构群]] 的群结构完全由矩阵群 $GL(2,\mathbb{C})$ 决定，可借助线性代数工具研究（例如用矩阵的迹判断默比乌斯变换的类型）。

## 出处

《数学指南——实用数学手册》1.14.11.5；相关概念见 [[复射影群]]。