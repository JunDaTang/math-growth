---
type: query
title: "Research: 局部-整体原理（Hasse principle）的现代推广与反例"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: 局部-整体原理（Hasse principle）的现代推广与反例

# 局部-整体原理（Hasse principle）的现代推广与反例

## 概述

**局部-整体原理**（local-global principle），通称 **Hasse 原理**，是丢番图几何与代数数论中的核心判据：一个定义在整体域（如 $\mathbb{Q}$ 或更一般的数域）上的代数簇 $X$，其有理点集 $X(\mathbb{Q})$ 非空，当且仅当它在所有局部域上的点集 $X(\mathbb{Q}_v)$ 均非空，即 $X(\mathbb{Q}) \neq \varnothing \iff X(\mathbb{Q}_v) \neq \varnothing$ 对所有位 $v$ 成立（$v$ 遍历实数位与全部 $p$ 进位）。换言之，"处处局部可解"是否蕴含"整体可解"，构成了局部-整体原理的判定问题 [8][9]。

这一原理并非普遍成立。对低次（二次）对象它成立，对三次及更高次对象则频繁失效。围绕这些失效，现代数论发展出了以 **Brauer–Manin obstruction**（Brauer–Manin 障碍）为代表的一整套障碍理论，用以刻画"局部可解但不整体可解"的机制，并把原理推广到整点、嵌入问题等更广的设定 [7][8][9]。

## 经典正例：Hasse–Minkowski 定理

局部-整体原理的第一个重大肯定性结果是 **Hasse–Minkowski 定理**：一个二次型在数域上非平凡地表示零，当且仅当它在数域的所有完备化上非平凡地表示零。也就是说，对二次型（二次超曲面，quadrics）而言，局部-整体原理成立 [9]。

Hasse–Minkowski 定理因此成为整个领域的"基准情形"：它表明原理至少在二次层面是完备的，从而把研究的焦点转向次数更高的形式与曲面，寻找其失效之处 [9]。

## 经典反例：Selmer 曲线 $3x^3+4y^3+5z^3=0$

最常见的失效例子是 **Selmer 曲线**
$$3x^3 + 4y^3 + 5z^3 = 0,$$
它是一条光滑平面三次曲线（亏格 1），被广泛引用为 Hasse 原理失效的经典范例 [11][12][13]。它的关键性质是：

- 该方程在实数域 $\mathbb{R}$ 中与所有 $p$ 进域 $\mathbb{Q}_p$ 中都有非平凡解，即在 $\mathbb{Q}$ 的所有完备化中均可解 [12][15]；
- 但它在 $\mathbb{Q}$ 上没有非平凡有理点，因而 Hasse 原理失效 [11][13]。

具体地，Keith Conrad 的讲义给出了各局部解的存在性构造：在 $\mathbb{R}$ 中有解 $\left(\sqrt[3]{5/3},\,0,\,-1\right)$；在 $\mathbb{Q}_3$ 中有形如 $(0,\,y,\,-1)$ 的解，其中 $y^3 = 5/4$；Luis Modes 的材料进一步验证了该曲线在 $\mathbb{Q}$ 的全部完备化（$\mathbb{R}$ 及所有 $p<\infty$ 的 $\mathbb{Q}_p$）中都有解 [12][15]。Stack Exchange 的讨论补充说明该方程在任意 $2$ 的幂与任意 $3$ 的幂模意义下均可解 [13]。相关的 $(3,4,5)$ 系数结构也被整理为习题，用于证明形如 $3x^3+4y^3=5$ 的方程在任意 $\mathbb{Q}_p$ 中有解 [14]。

Selmer 曲线表明：一旦从二次型升至三次（或更高次）形式，局部-整体原理就可能崩塌 [11][12][13]。

## 三次曲面上的失效：Mordell 与 Swinnerton-Dyer

比曲线更"高维"的对象是三次曲面（cubic surfaces）。相关历史与结果包括：

- **Mordell 的构造**：Mordell 构造了使 Hasse 原理失效的三次曲面，这是该领域较早的反例来源 [4]。
- **Swinnerton-Dyer 的存在性结果**：Swinnerton-Dyer 证明了在 $\mathbb{Q}$ 上存在光滑三次曲面 $V \subset \mathbb{P}^3$，使得 Hasse 原理失效 [5]。基于这一存在性，后续工作进一步构造出显式的、违背局部-整体原理的亏格一曲线代数族 [5]。

这些结果把失效现象从单条曲线推广到一整类曲面与曲线族，说明 Hasse 原理的失效并非孤立偶然，而是三次几何中具有结构性的现象 [4][5]。

## 现代推广：Brauer–Manin obstruction

为解释局部-整体原理的失效，现代理论引入了 **Brauer–Manin obstruction**（亦称 **Manin obstruction**）。其思想是：在 adele 环上的点集 $X(\mathbb{A}_\mathbb{Q})$ 上，利用 $X$ 的 Brauer 群 $\mathrm{Br}(X)$ 的作用构造出一个子集 $X(\mathbb{A}_\mathbb{Q})^{\mathrm{Br}}$，满足
$$X(\mathbb{Q}) \subseteq X(\mathbb{A}_\mathbb{Q})^{\mathrm{Br}} \subseteq X(\mathbb{A}_\mathbb{Q}).$$
当 $X(\mathbb{A}_\mathbb{Q})$ 非空而 $X(\mathbb{A}_\mathbb{Q})^{\mathrm{Br}}$ 为空时，即得到对局部-整体原理的阻碍 [7][8][9]。这一框架把"处处局部可解却无整体点"的现象纳入一个统一的算术障碍体系 [8]。

关于此障碍的强度：

- 对**阿贝尔簇**，Manin 障碍本质上就是 **Tate–Shafarevich 群**，并且在（相应有限性假设下）能够**完全解释**局部→整体原理的失效 [7]。
- 对一般簇，Manin 障碍是否**唯一**的障碍（即是否存在 Brauer–Manin 无法捕捉的失效）仍是一个中心问题；有工作专门讨论局部-整体障碍的**有限性**问题 [9]。

## 更进一步的推广

### 整（integral）Hasse 原理

Hasse 原理可推广到**整点**（即要求解为整数坐标）的情形，即整 Hasse 原理。相关研究针对**仿射对角三次曲面**（affine diagonal cubic surfaces）发展了**整 Brauer–Manin 障碍**，并据此构造出**第一批违反整 Hasse 原理的反例** [3]。这表明现代推广不仅涉及有理点，也延伸到整点这一更精细的层次 [3]。

### 嵌入问题

另一类推广是把局部-整体原理（及其 Brauer–Manin 障碍）从"点的存在性"推广到**嵌入问题**（embedding problems）上。相关工作研究了整体域上嵌入问题的 Brauer–Manin 障碍的类比版本，并证明了与之对应的定理 [6][10]。

### 高次形式

对**高次形式**（forms of large degree）表示零的问题，Hasse 原理一般不成立；研究焦点之一即 Understanding 其 Brauer–Manin 障碍以及障碍本身的有限性 [9]。

## 反例的稠密性

一个反映失效现象普遍性的现代结果指出：**违反 Hasse 原理的三次曲面在非奇异三次曲面的模空间（moduli scheme）中是 Zariski 稠密的** [1]。也就是说，在非奇异三次曲面的参量空间中，满足局部-整体原理失败的对象并非某种"测度为零"的例外，而是以 Zariski 拓扑意义下的"稠密"方式分布，进一步印证了三次层面局部-整体原理失效的广泛性与结构性 [1][4]。

## 矛盾与空白

- **障碍的完备性存疑**：对阿贝尔簇，Manin 障碍（Tate–Shafarevich 群）在相应假设下可完全解释失效 [7]；但对一般簇，Brauer–Manin 障碍是否为**唯一**障碍尚无定论，"障碍有限性"仍是开放议题 [9]。这些来源之间在"是否能完全解释失效"上的适用范围差异，需要注意区分。
- **有理点 vs. 整点**：传统 Hasse 原理讨论有理点，而整 Hasse 原理的反例（仿射对角三次曲面）相对更晚才被构造出来 [3]，两类结果的几何设定不可直接互推。
- **一般性推广的边界**：嵌入问题 [6][10] 与高次形式 [9] 的推广尚属活跃研究领域，其障碍与经典 Brauer–Manin 的对应强度仍需进一步厘清。
- **构造性 vs. 存在性**：Swinnerton-Dyer 给出的是存在性定理，显式代数族由后续工作补足 [5]；而 Selmer 曲线等则提供了可直接验证的显式反例 [11][12][15]。两类证据的"可验证性"层级不同。

## 建议的额外来源

1. Skorobogatov 关于 Brauer–Manin 障碍与局部-整体原理的专著或综述，以系统化障碍框架。
2. Manin 原始论文，用于追溯 "Manin obstruction" 的提出与 Tate–Shafarevich 群的对应。
3. 关于三次曲面模空间几何（moduli of cubic surfaces）的文献，以理解 Zariski 稠密性结果 [1] 的技术背景。
4. 关于整 Hasse 原理与整 Brauer–Manin 障碍的后续论文 [3]，以及仿射对角三次曲面的整点理论。

---

**引用来源**：[1] Cubic surfaces violating the Hasse principle are Zariski dense…；[2] MathOverflow: Cubic forms and Hasse Principle；[3] arXiv: Cubic surfaces failing the integral Hasse principle；[4] EuDML: More cubic surfaces violating the Hasse principle；[5] MIT PDF: an explicit algebraic family of genus-one curves violating the Hasse principle；[6] arXiv: The Brauer-Manin obstruction… for embedding problems；[7] Wikipedia: Manin obstruction；[8] Michigan thesis: Local-global problems and the Brauer-Manin obstruction；[9] MathOverflow: Hasse principle and Brauer-Manin obstruction for forms of large degree；[10] World Scientific: Brauer–Manin obstruction… embedding problems；[11] MathOverflow: Proof of no rational point on Selmer's Curve $3x^3+4y^3+5z^3=0$；[12] Keith Conrad: Selmer's example；[13] Math StackExchange: On the equation $3x^3+4y^3+5z^3=0$；[14] Imperial College: Number Theory Problem Sheet 3；[15] Luis Modes: Some exceptions to the local-global principle。

## References

1. [Cubic surfaces violating the Hasse principle are Zariski dense in the ...](https://www.sciencedirect.com/science/article/pii/S0001870815001565) — sciencedirect.com
2. [Cubic forms and Hasse Principle - MathOverflow](https://mathoverflow.net/questions/143789/cubic-forms-and-hasse-principle) — mathoverflow.net
3. [Cubic surfaces failing the integral Hasse principle - arXiv](https://arxiv.org/html/2311.10008v2) — arxiv.org
4. [More cubic surfaces violating the Hasse principle - EuDML](https://eudml.org/doc/219781) — eudml.org
5. [[PDF] an explicit algebraic family of genus-one curves violating the ...](https://math.mit.edu/~poonen/papers/cubics.pdf) — math.mit.edu
6. [The Brauer-Manin obstruction to the local-global principle for the ... - arXiv](https://arxiv.org/abs/1602.04998) — arxiv.org
7. [Manin obstruction - Wikipedia](https://en.wikipedia.org/wiki/Manin_obstruction) — en.wikipedia.org
8. [Local -global problems and the Brauer -Manin obstruction.](https://deepblue.lib.umich.edu/items/07656b2f-2ec1-4d4e-9e91-3eb1aa6bbc9a) — deepblue.lib.umich.edu
9. [Hasse principle and Brauer-Manin obstruction for forms of large degree](https://mathoverflow.net/questions/163055/hasse-principle-and-brauer-manin-obstruction-for-forms-of-large-degree) — mathoverflow.net
10. [Brauer–Manin obstruction to the local–global principle for the embedding ...](https://www.worldscientific.com/doi/10.1142/S1793042122500786?srsltid=AU7gw4XO1sKTasT53T99G8oo7Psz-D62_s9--GAG2AaayOJwfw2PVFdr) — worldscientific.com
11. [Proof of no rational point on Selmer's Curve $3x^3+4y^3+5z^3=0](https://mathoverflow.net/questions/2779/proof-of-no-rational-point-on-selmers-curve-3x34y35z3-0) — mathoverflow.net
12. [[PDF] selmer's example - keith conrad](https://kconrad.math.uconn.edu/blurbs/gradnumthy/selmerexample.pdf) — kconrad.math.uconn.edu
13. [On the equation $3x^3 + 4y^3 + 5z^3 = 0$ - Mathematics Stack Exchange](https://math.stackexchange.com/questions/55119/on-the-equation-3x3-4y3-5z3-0) — math.stackexchange.com
14. [[PDF] Number Theory: Elliptic Curves, Problem Sheet 3](https://www.ma.imperial.ac.uk/~tsg/Index_files/ellcurves3.pdf) — ma.imperial.ac.uk
15. [[PDF] Some exceptions to the local-global principle - Luis Modes](https://luismodes.com/docs/18.782%20Final%20Paper%20%20(Luis%20Modes).pdf) — luismodes.com

## Related
- [[queries/research-hasse-principle-的现代推广与反例-2026-09-27-160545-research-1]]
