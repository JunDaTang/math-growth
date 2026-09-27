---
type: query
title: "Research: p 进数（p-adic numbers）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: p 进数（p-adic numbers）

# p 进数（p-adic numbers）

## 概述

**p 进数**（英语：p-adic number，亦称局部数体）是数论中的核心概念，指有理数域 $\mathbb{Q}$ 相对于某个固定素数 $p$ 所定义的"进绝对值"进行完备化后得到的完备数域，通常记作 $\mathbb{Q}_p$ [7][8]。它是有理数域 $\mathbb{Q}$ 的若干种完备化之一，与实数域 $\mathbb{R}$ 来源于 $\mathbb{Q}$ 关于通常绝对值（阿基米德绝对值）的完备化相互平行 [2][8]。

p 进数的核心思想在于：它给出了定义"两个有理数之间距离"的另一种方式 [2]。在这种度量下，两个数彼此"接近"，意味着它们的差能被素数 $p$ 的高次幂整除 [5]。换言之，模 $p$ 的幂的同余关系与所谓的 p 进度量下的邻近性被直接联系起来 [5]——这正是 p 进数区别于实数而独具价值之处。

p 进数由 K. 亨泽尔（K. Hensel）于 **1902 年**首次提出，由此开启了代数数论中"局部化方法"的研究 [7]。

## p 进赋值与 p 进绝对值

**p 进赋值**（p-adic valuation，又称 p 进阶）是定义 p 进距离的基础工具。对整数 $n$，其 p 进赋值 $v_p(n)$ 定义为**能整除 $n$ 的 $p$ 的最高次幂的指数** [4]。这一赋值可以自然地延拓到有理数域：对 $x = a/b \in \mathbb{Q}$，有 $v_p(a/b) = v_p(a) - v_p(b)$。

由此可定义 **p 进绝对值** $|x|_p = p^{-v_p(x)}$。该绝对值具有**乘性**（multiplicativity），并满足**非阿基米德**的强三角不等式 $|x+y|_p \le \max(|x|_p, |y|_p)$ [7][13]。乘性是非阿基米德绝对值的一个关键条件——[14] 特别提醒，Ostrowski 定理的成立实质上需要依赖乘性这一（第 4 个）条件，而该条件在某些通俗讲解中常被遗漏 [14]。

## 数域 $\mathbb{Q}_p$ 的构造与性质

p 进数域又称**局部数域**，是数域关于 p 进绝对值的完备化 [7]。其构造方式与实数域类似：将 $\mathbb{Q}$ 按 p 进度量取柯西序列的完备化。由于 p 进绝对值是非阿基米德的，$\mathbb{Q}_p$ 因此具有一系列与 $\mathbb{R}$ 显著不同的性质（例如其上不存在通常意义的阿基米德序结构）。

$\mathbb{Q}_p$ 中的元素可视为"以 $p$ 为基"的形式级数，其"整数部分"构成环 $\mathbb{Z}_p$（p 进整数环）。与实数分析相类，p 进数上同样可以建立一套分析学（p 进分析），其中涉及 Haar 测度等概念——这部分与 [[测度论]] 的思想一脉相承。p 进数不仅与数论密切相关，也在分析、代数等多个数学分支中发挥作用 [2]。

## Ostrowski 定理

**Ostrowski 定理**（Alexander Ostrowski，1916 年）刻画了有理数域上所有可能的绝对值 [11]。其核心结论是：

> 有理数域 $\mathbb{Q}$ 上每一个非平凡绝对值，都等价于通常的实数绝对值，或等价于某一个 p 进绝对值 [11][15]。

该定理说明了实数绝对值与 p 进绝对值在数域上的**唯一性与穷尽性**，是理解 p 进数"为何如此"的关键定理。

Ostrowski 定理可推广到数域：对任意数域 $K$，其每一个非平凡绝对值都等价于某个素理想 $\mathfrak{p}$ 对应的 p 进绝对值（对 $O_K$ 中唯一的素数 $\mathfrak{p}$），或等价于一个阿基米德绝对值 [12]。

## 局部-整体原则（Hasse 原理）

**局部-整体原则**（local-global principle，又称 **Hasse 原理**）是数论中的一种重要数学策略：通过验证方程在"局部"域（实数域 $\mathbb{R}$ 以及所有 p 进数域 $\mathbb{Q}_p$）中是否存在解，来判定其在有理数域 $\mathbb{Q}$ 上是否存在"整体"解 [9]。该原则在**二次型**领域由哈塞（Hasse）给出 [9]。

局部-整体原则之所以能借助 p 进数发挥作用，源自一个更深的直觉（见 [10] 的一则讨论）：

> 在某些情况下，已知这个问题可以被忽略，并且可以使用 p 进数完全解决这个问题。这些被称为局部-整体原则。但困难的部分是当你不能忽略这个问题的时候。

也就是说，当局部可解确实蕴含整体可解时，p 进数提供了完整而有力的工具；而当这一蕴含关系失效（所谓"局部-整体原则的障碍"）时，问题的困难恰恰集中于此 [10]。

## p 进数的代数性质与应用

p 进数在现代数论中无处不在 [1]，其应用横跨数论、分析与代数等领域 [2]。主要方向包括：

- **代数数论**：p 进赋值、p 进域是研究素理想分解、单位群等问题的基本语言；[3] 讨论的"p 进代数数"（field of p-adic algebraic numbers）即指由 $\mathbb{Q}$ 上代数元构成的 p 进域，可理解为 $\mathbb{Z}_{(p)}$ 的 Hensel 化（Henselization）的分式域 [3]。
- **局部-整体方法**：借助 $\mathbb{Q}_p$ 与 $\mathbb{R}$ 这一族"局部域"，把整体问题分解为若干局部问题处理 [6][9]。
- **函数域类比**：数域与函数域之间存在"亲兄弟"式的类比，局部域与整体域的框架、以及局部-整体原则在其中均有对应 [6]。

## 关于 p 进数的经典数论应用

作为数论中最富魅力的对象之一 [1]，p 进数及其紧密相关的**赋值论**（theory of valuations）共同构成了现代数论的基础设施。正如 [1] 所提出的问题——"p 进数为何在现代数论中无处不在"——其答案正根植于 Ostrowski 定理（赋值的完全分类）与局部-整体方法（把整体问题局部化）这两条主线之中 [1][11][9]。

## 争议、空白与待核实之处

1. **权威性来源不足**：现有材料多为百科条目、讲义 PDF 与问答社区讨论（[1]–[15]），缺少一部系统教材或原始文献作为权威支撑。p 进数的严格构造（柯西序列完备化 / 逆向极限两种等价途径）在现有来源中均未完整给出，属于明显空白。
2. **Hensel 提出年份**：[7] 记为 1902 年，此点与主流数论史叙述一致，但由于仅有单一来源（百度百科），建议以权威文献交叉核对。
3. **Ostrowski 定理的完整陈述**：[11] 与 [15] 给出的是对 $\mathbb{Q}$ 的版本，[12] 给出数域版本，但各来源对"等价"的定义及阿基米德情形的处理细节存在繁简差异，需以 [12] 一类讲义的完整证明为准 [11][12]。
4. **局部-整体原则的适用边界**：[9] 与 [10] 均指出该原则并非普遍成立，存在"不能忽略障碍"的情形，但现有来源未给出具体反例（如经典的 Selmer 型反例），此处存在内容缺口 [9][10]。
5. **术语一致性**："p 进数域"（[7]）、"局部数域"（[7]）、"p 进代数数"（[3]）等术语在不同来源中用法略有差异，需在使用时明确所指。

## 进一步值得查找的来源

为弥补上述空白，建议补充以下类型的权威来源：

- 系统教材：Gouvêa《p-adic Numbers: An Introduction》；Koblitz《p-adic Numbers, p-adic Analysis, and Zeta-Functions》；Serre《A Course in Arithmetic》。
- 原始文献：Hensel（1902）关于 p 进数的开创性论文；Ostrowski（1916）原始论文。
- 局部-整体原则专题：Hasse–Minkowski 定理的严格陈述，以及局部-整体原则失效的具体反例文献。
- 中文权威材料：一本中文数论或代数数论教材，以核对 [7][8] 中的译名与年份。

## 参考来源

- [1] Classical number theoretic applications of the $p$-adic numbers（math.stackexchange.com）
- [2] An Introduction to the p-adic Numbers（math.uchicago.edu，PDF）
- [3] Which p-adic numbers are also algebraic?（mathoverflow.net）
- [4] p-adic valuation（en.wikipedia.org）
- [5] p-adic Number（Wolfram MathWorld）
- [6] 数论（6）——p 进数和局部-整体原则（知乎专栏）
- [7] P 进数域（百度百科）
- [8] p進數（中文维基百科）
- [9] 局部-整体原则（Bohrium）
- [10] 关于"p 进数试图告诉我们一些非常深刻的东西"的讨论（Reddit）
- [11] Ostrowski's theorem（en.wikipedia.org）
- [12] Ostrowski for number fields（Keith Conrad，讲义 PDF）
- [13] Identify absolute values in Ostrowski's theorem for number fields（math.stackexchange.com）
- [14] Ostrowski's Theorem (p-adic metric continued)（YouTube）
- [15] Every non-trivial absolute value on the rational numbers is equivalent to ...（x.com）

## References

1. [Classical number theoretic applications of the $p$-adic numbers](https://math.stackexchange.com/questions/3951500/classical-number-theoretic-applications-of-the-p-adic-numbers) — math.stackexchange.com
2. [[PDF] AN INTRODUCTION TO THE p-ADIC NUMBERS](http://math.uchicago.edu/~may/REU2020/REUPapers/Pomerantz.pdf) — math.uchicago.edu
3. [Which p-adic numbers are also algebraic? - MathOverflow](https://mathoverflow.net/questions/17032/which-p-adic-numbers-are-also-algebraic) — mathoverflow.net
4. [p-adic valuation - Wikipedia](https://en.wikipedia.org/wiki/P-adic_valuation) — en.wikipedia.org
5. [p-adic Number -- from Wolfram MathWorld](https://mathworld.wolfram.com/p-adicNumber.html) — mathworld.wolfram.com
6. [数论（6）——p进数和局部-整体原则 - 知乎专栏](https://zhuanlan.zhihu.com/p/40898123) — zhuanlan.zhihu.com
7. [P 进数域_百度百科](https://baike.baidu.com/item/P%20%E8%BF%9B%E6%95%B0%E5%9F%9F/15681116) — baike.baidu.com
8. [𝑝進數- 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/P%E9%80%B2%E6%95%B8) — zh.wikipedia.org
9. [局部-整体原则| Bohrium](https://www.bohrium.com/sciencepedia/feynman/keyword/local_to_global_principle) — bohrium.com
10. [我听说一个教授说：“p进数试图告诉我们一些非常深刻的东西 ... - Reddit](https://www.reddit.com/r/math/comments/11tvem1/i_heard_a_professor_say_the_padics_are_trying_to/?tl=zh-hans) — reddit.com
11. [Ostrowski's theorem - Wikipedia](https://en.wikipedia.org/wiki/Ostrowski%27s_theorem) — en.wikipedia.org
12. [[PDF] Ostrowski for number fields - Keith Conrad](https://kconrad.math.uconn.edu/blurbs/gradnumthy/ostrowskinumbfield.pdf) — kconrad.math.uconn.edu
13. [Identify absolute values ​in Ostrowski's theorem for number fields](https://math.stackexchange.com/questions/5040009/identify-absolute-values-in-ostrowskis-theorem-for-number-fields) — math.stackexchange.com
14. [Ostrowski's Theorem (p-adic metric continued) - YouTube](https://www.youtube.com/watch?v=aSxvz0NUXfc) — youtube.com
15. [Every non-trivial absolute value on the rational numbers is equivalent to ...](https://x.com/AlgebraFact/status/1930279673981788295) — x.com
