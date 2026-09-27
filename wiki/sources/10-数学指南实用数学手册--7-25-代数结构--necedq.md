---
type: source
title: 《数学指南——实用数学手册》2.5 代数结构
created: 2026-09-27
updated: 2026-09-27
tags: [数学指南, 代数结构, 群, 环, 域, 抽象代数]
related: [concepts/群, concepts/环, concepts/域与体, concepts/伽罗瓦理论, concepts/可解群, concepts/高斯剩余类环, concepts/复数域的哈密顿构造]
sources: ["数学指南_实用数学手册/2.5 代数结构.md"]
authors: []
year: 0
url: ""
venue: ""
---

# 《数学指南——实用数学手册》2.5 代数结构

## 概述

本节把在实数上可进行的加法与乘法推广到一般数学对象，由此引出 **群、环、域** 三个基本代数结构。这些概念产生于 19 世纪解代数方程以及解决数论与几何问题的过程。核心脉络是：群刻画对称性 → 群论结果（如 [[concepts/可解群]]）经 [[concepts/伽罗瓦理论]] 判定代数方程是否可用根式解 → 环与域刻画加法与乘法的整体规律。

## 2.5.1 群

群是一集合，集合中任意有序对 $(g,h)$ 均有乘积 $gh$，并满足三条公理：

```
(i) 结合律: g(hk) = (gh)k
(ii) 中性元素: 存在唯一 e 使 eg = ge = g
(iii) 逆元素: 对每个 g 存在唯一 g^{-1} 使 gg^{-1} = g^{-1}g = e
```

满足 $gh = hg$ 的群称为交换群（阿贝尔群）。给出三类典型例子：数群（非零实数乘法群）、矩阵群（[[concepts/群]] 中 $GL(n,\mathbb{R})$、三维旋转群）、[[concepts/变换群]] 与 [[concepts/置换群-对称群]] $S_n$。引入对换、[[concepts/置换的符号]] 与循环置换，并给出

$$
\operatorname{sgn}(\pi_1\pi_2) = \operatorname{sgn}\pi_1 \operatorname{sgn}\pi_2 \tag{2.61}
$$

### 2.5.1.1 子群

[[concepts/子群]] 定义等价于 $gh^{-1}\in H$。[[concepts/正规子群]] 要求 $ghg^{-1}\in H$；[[concepts/单群]] 只有平凡正规子群；[[concepts/拉格朗日阶定理]] 指出有限群子群的阶整除群的阶。给出 [[concepts/交错群]] $\mathcal{A}_n$ 及 $S_2,S_3,S_4$ 的正规子群结构（含克莱因交换四元群 $\mathcal{K}_4$）。[[concepts/加法群]] 是把运算写作 $+$、中性元素写作 $0$ 的交换群。

### 2.5.1.2 群同态

[[concepts/群同态与同构]] 定义为保运算映射 $\varphi(gh)=\varphi(g)\varphi(h)$；[[concepts/自同构群]] $\operatorname{Aut}(G)$ 与内自同构 $\varphi_g(h)=ghg^{-1}$；[[concepts/商群]] $G/N$ 满足

$$
\mathrm{ord}(G/N) = \frac{\mathrm{ord}\,G}{\mathrm{ord}\,N}
$$

**群同态的结构定理** 与两条 [[concepts/群同态的结构定理与同构律]]：$H\cong G/\ker\varphi$、$HN/N\cong H/(H\cap N)$、$G/H\cong(G/N)/(H/N)$。

### 2.5.1.3 循环群与主定理

[[concepts/循环群]] $g=a^n$；每个循环群是交换的，每个素数阶有限群是循环群。[[concepts/加法群的主定理]] 给出有限生成加法群的直和分解与秩、挠系数、[[concepts/加法群的主定理]] 中提到的贝蒂数。

### 2.5.1.4 可解群

[[concepts/可解群]] 由子群链 $G_0\subseteq\cdots\subseteq G_n=G$ 定义，其中 $G_j\trianglelefteq G_{j+1}$ 且 $G_{j+1}/G_j$ 交换。$S_2,S_3,S_4$ 可解，$n\ge5$ 时 $S_n$ 不可解，这构成次数 $\ge5$ 方程不可根式解的依据（见 2.6.5）。

## 2.5.2 环

[[concepts/环]] 是加法群且带满足结合律与分配律的乘法。交换环、单位元、[[concepts/整环]] 与零因子、子环、[[concepts/理想与商环]]、[[concepts/多项式环]] $P[x]$、环同态与商环 $R/J$。[[concepts/高斯剩余类环]] $\mathbb{Z}/m\mathbb{Z}$ 给出记号

```
z ≡ w mod m   ⇔   z - w 被 m 整除
```

并讨论 $m=2,3,4$ 的例子（$m=4$ 有零因子）；$\mathbb{Z}/m\mathbb{Z}$ 无零因子当且仅当 $m$ 为素数。环同态结构定理：$\ker\varphi$ 是理想且 $S\cong R/\ker\varphi$。

## 2.5.3 域

[[concepts/域与体]]：体是加群且 $K-\{0\}$ 是乘法群且 $K$ 是环；域是乘法交换的体。方程 $ax=b$、$ya=b$、$c+z=d$ 有唯一解。[[concepts/域的特征与素域]]、[[concepts/伽罗瓦域]]（有限体，元素个数为 $p^n$）。

[[concepts/复数域的哈密顿构造]]：以有序对 $(a,b)$ 定义加法与乘法，$\mathrm{i}:=(0,1)$，得到

```
(a,b)+(c,d) = (a+c, b+d)
(a,b)(c,d) = (ac-bd, ad+bc)
i^2 = -1
```

[[concepts/商域-分式域]] $Q(P)$ 的构造（等价类 $[(a,b)]$）与 [[concepts/有理函数域]] $P(x)$。

## 结构线索

- 群 → 子群/正规子群/单群 → 同态结构定理与同构律 → 商群
- 可解群 + 伽罗瓦理论 → 五次以上方程无根式解
- 环 → 理想 → 商环 → 域（素数模剩余类环给出有限域）
- 域 → 特征与素域 → 伽罗瓦域；哈密顿有序对构造给出 $\mathbb{C}$ 与四元数体