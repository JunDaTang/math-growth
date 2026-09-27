---
type: finding
title: 维拉索罗代数 W 的构造与中心扩张 Vir
source: "[[10-数学指南实用数学手册--7-244-李代数--5tba6c]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [李代数, 维拉索罗代数, 中心扩张]
related: [维拉索罗代数, 中心扩张-李代数, 李代数, 维拉索罗]
sources: ["数学指南_实用数学手册/2.4.4 李代数.md"]
---

# 维拉索罗代数 W 的构造与中心扩张 Vir

## 陈述

源文通过三步构造维拉索罗代数：

**第一步（函数空间）**：设 $C^{\infty}(S^{1})$ 表示单位圆 $S^{1} := \{z \in \mathbb{C} : |z| = 1\}$ 上的所有在原点附近正则的函数 $f : S^{1} \to \mathbb{C}$ 的线性空间（源文带脚注标记 $^{1)}$）。

**第二步（算子与子代数 W）**：令

$$
L_{n}(f) := - z^{n+1} \frac{\mathrm{d} f}{\mathrm{d} z}, \quad n = 0, \pm 1, \pm 2, \dots .
$$

如果 $W$ 表示所有 $L_{n}$ 的复线性包，那么关于方括号

$$
[ L_{n}, L_{m} ] = (n - m) L_{n + m}, \quad n, m = 0, \pm 1, \pm 2, \dots ,
$$

$W$ 是一个无穷维复李代数，且 $[L_n, L_m] = L_n L_m - L_m L_n$。

**第三步（中心扩张）**：取 1 维复线性空间 $Y := \operatorname{span}\{Q\}$，关于乘积

$$
\boxed{
\begin{array}{l}
[ L_{n}, L_{m} ] = (n - m) L_{n + m} + \delta_{n, -m} \dfrac{n^{3} - n}{12} Q, \quad n, m = 0, \pm 1, \dots ,\\
[ L_{n}, Q ] = 0,
\end{array}}
\tag{Vir}
$$

外直和 $\operatorname{Vir} := W \oplus Y$ 成为一个无穷维复李代数，称为维拉索罗代数；源文明确指出它是 $W$ 的一个中心扩张（同样带脚注标记 $^{1)}$）。

## 物理意义断言

源文断言：维拉索罗代数在现代弦理论和保形理论中起着极其重要的作用。该断言在源文中未附进一步说明或引用细节，故本页仅如实记录，不扩展。

## 相关页面

- [[维拉索罗代数]]、[[中心扩张-李代数]]、[[李代数]]
