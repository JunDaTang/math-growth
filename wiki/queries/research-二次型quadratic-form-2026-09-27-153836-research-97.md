---
type: query
title: "Research: 二次型（Quadratic Form）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 二次型（Quadratic Form）

# 二次型（Quadratic Form）

## 概述

二次型（Quadratic Form）是代数学中的核心对象，其研究贯穿线性代数、数论、代数几何与拓扑学。在本 wiki 已有的数理统计与概率论语料中，二次型多以协方差阵、广义高斯分布指数项等形式隐式出现（参见 [[协方差阵]]、[[广义高斯分布]]、[[卡方分布]]），而本次收集的五个来源则集中于二次型的代数与算术理论，尤其是围绕 **Witt 群（Witt group）** 与 **Witt 环（Witt ring）** 的分类框架 [1][5]。

n 元二次型即在给定域 K 上的 n 元齐次二次多项式；更抽象地，它可被视作带有双线性形式或对称结构的「二次空间」。围绕这一对象发展出的分类理论，构成了二次型理论的主干。[5]

## 二次型的四种等价定义

据 UGA 数学系的讲义《Quadratic Forms Chapter I: Witt's Theories》，二次型有四种彼此等价的定义方式，这一「四重等价」是 Witt 理论的出发点 [5]。讲义随后讨论群 $M_n(K)$ 对 n 元二次型的**作用（action）**，并建立**二次空间范畴（the category of quadratic spaces）** [5]。这一范畴化的视角使得二次型可以用范畴论与同调代数工具处理，是通向 Witt 群定义的桥梁。

> 说明：当前来源 [5] 仅给出讲义的目录与章节标题，四种定义的具体内容、$M_n(K)$ 作用的形式以及二次空间范畴的射（morphism）定义均未在收集材料中展开，属待补充的空白。

## Witt 群与 Witt 环

Witt 群的基本思想是：在二次型（或二次空间）的集合上按某种等价关系取商，使其构成一个群，从而对二次型进行分类 [1][5]。

**Witt 环（Witt ring）** 则在群结构之上进一步引入加法与乘法的相容结构（即环结构），常见于数域（number field）情形下——来源 [1] 特别提到「number field 的 Witt 环」[1]。与 Witt 环密切相关的是 **Grothendieck–Witt 环（Grothendieck–Witt ring）**，两者是二次型算术理论中的基本不变量 [1]。

值得注意的是，Witt 群的定义方式并不限于对称双线性形式：它同样定义于**斜对称形式（skew-symmetric forms）**、**二次型（quadratic forms）**，乃至更一般的 **ε-二次型（ε-quadratic forms）**，且可以在任意 **\*-环（\*-ring）R** 上建立 [1]。这体现了该构造的普适性。

## 域关于二次型的等价分类

来源 [3] 的主题是「Witt 群与域关于二次型的等价性」（The Witt Group and the Equivalence of Fields with Respect to Quadratic Forms）。该研究利用若干过程，对所有满足条件 $q \sim 8$ 的**非实域（nonreal fields）**进行了等价分类，并刻画了具有「每个可能值……」这一性质的域 [3]。

> 说明：来源 [3] 仅有摘要片段，其中「$q \sim 8$」的确切含义（是否为某个不变量取值、序数或域类标记）以及「每个可能值」性质的完整陈述均不清晰，需查阅原文核实。这是本主题的一处明显缺口。

## 整数上的扩展二次型与 Q-形式

arXiv 论文 2404.09189《The Witt groups of extended quadratic forms over Z》研究**整数上的二次型参数 Q** 以及取值于 Q 的**扩展二次型（extended quadratic forms）**，作者将后者称为 **Q-形式（Q-forms）**，并研究其 Witt 群 [2]。

这一类研究的动机通常来自整数环 $\mathbb{Z}$ 上二次型的算术性质：当标量环从域退化为 $\mathbb{Z}$ 这样的环时，Witt 群的结构变得更加复杂，需要引入「扩展」「参数化」等概念来处理。[2]

## 局部环上的上同调不变量

来源 [4]《Cohomological invariants of quadratic forms over local rings》讨论局部环上二次型的**上同调不变量（cohomological invariants）** [4]。其技术核心是：对任意**非分歧正则局部环（unramified regular local ring）** 的 Witt 群，证明 **Gersten 猜想（Gersten conjecture）**（见该文定义 2.2）[4]。

这一结果的意义在于把二次型的 Witt 群理论从域的情形推广到更一般的环的情形，并与代数 K 理论中的 Gersten 猜想传统相接。所用的方法在摘要中被概述为「使用……的方法」，但具体技术手段有待查阅正文 [4]。

## 与现有 wiki 条目的联系

- 二次型与**协方差阵**密切相关：样本协方差阵的二次型 $\mathbf{x}^{\mathsf{T}} S \mathbf{x}$ 是多元统计推断的基础（参见 [[协方差阵]]、[[多元分析]]）。
- **广义高斯分布**的概率密度指数项即为二次型（参见 [[广义高斯分布]]）。
- 正态变量的二次型分布构成了 **χ² 分布** 的来源（参见 [[卡方分布]]、[[t分布]]、[[F分布]]）。
- 上述统计应用与本文所讨论的 Witt 群框架属于二次型理论的两个不同侧面：前者是实/复域上的解析与概率应用，后者是数论与代数上的分类理论。

## 矛盾、缺口与待澄清之处

1. **缺少基础定义来源**：现有五个来源均未给出二次型的初等定义与矩阵表示（$Q(x) = x^{\mathsf{T}} A x$ 形式），也未覆盖正定性、标准形、惯性定理等经典内容。二次型的基本代数理论在本 wiki 中尚属空白。
2. **来源 [5] 仅为目录**：四种等价定义、$M_n(K)$ 作用与二次空间范畴的具体内容缺失。
3. **来源 [3] 的记号不明**：$q \sim 8$ 与「每个可能值」性质的精确表述不清楚。
4. **来源 [1] 为百科条目片段**：Witt 群在斜对称形式、ε-二次型、\*-环上的统一定义未给出形式化陈述。
5. **各来源之间尚无直接矛盾**，但因主题层次不同（基础定义 / 分类理论 / 环上推广 / 算术细化），尚未形成连贯的叙述链条。

## 建议补充的来源

- 关于二次型的初等与经典理论（矩阵表示、惯性定理、Witt 消去定理）的标准教材章节。
- Witt 环的公理化定义（含加法与乘法结构与理想 $I^n$）。
- Grothendieck–Witt 环与代数 K 理论中 $K_0$ 的关系。
- 关于 ε-二次型与 \*-环的统一处理（例如 Quebbemann–Scharlau 或 Knus 等人的工作）。
- Milnor 猜想及其后续（Voevodsky 关于 Witt 群与 Milnor K 理论的结果）。
- 关于实域的二次型理论与序（ordering）分类。

## 参考来源

- [1] Witt group — Wikipedia（Witt group / Witt ring / Grothendieck–Witt ring）
- [2] arXiv:2404.09189, *The Witt groups of extended quadratic forms over Z*（Q-forms）
- [3] *The Witt Group and the Equivalence of Fields with Respect to Quadratic Forms*（ScienceDirect）
- [4] J. A. Jacobson, *Cohomological invariants of quadratic forms over local rings*（Gersten conjecture for Witt groups）
- [5] *Quadratic Forms Chapter I: Witt's Theories*（UGA math department）

## References

1. [Witt group - Wikipedia](https://en.wikipedia.org/wiki/Witt_group) — en.wikipedia.org
2. [[2404.09189] The Witt groups of extended quadratic forms over Z](https://arxiv.org/abs/2404.09189) — arxiv.org
3. [The Witt Group and the Equivalence of Fields with Respect to Quadratic ...](https://www.sciencedirect.com/science/article/pii/0021869373900021/pdf?md5=5c807f82126ece2f8452cf0453191d5c&pid=1-s2.0-0021869373900021-main.pdf) — sciencedirect.com
4. [[PDF] Cohomological invariants of quadratic forms over local rings](https://jeremyallenjacobson.github.io/CohomologicalInvariants.pdf) — jeremyallenjacobson.github.io
5. [[PDF] Quadratic Forms Chapter I: Witt's Theories - UGA math department](http://alpha.math.uga.edu/~pete/quadraticforms.pdf) — alpha.math.uga.edu
