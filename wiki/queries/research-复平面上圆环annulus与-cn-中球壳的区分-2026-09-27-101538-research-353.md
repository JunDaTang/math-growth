---
type: query
title: "Research: 复平面上「圆环」（annulus）与 C^n 中球壳的区分"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 复平面上「圆环」（annulus）与 C^n 中球壳的区分

# 复平面上的「圆环」（annulus）与 ℂⁿ 中的球壳（spherical shell）

## 一、同一公式，两种几何体

中文文献里的「圆环」通常指复平面中由两个同心圆周界定的区域

$$A=\{z\in\mathbb{C}:a<|z|<b\}.$$

把同一个不等式直接搬到 $\mathbb{C}^n$（$n\ge2$）中，得到的是**球壳**（spherical shell / shell / annulus）：

$$\mathrm{Shell}_{r,R}=\{z\in\mathbb{C}^n:r<\|z\|<R\},$$

它在微分拓扑上形如 $S^{2n-1}\times(r,R)$，边界是两个球面。来源中这一对象有多种记法：$\mathrm{Shell}_{r,r+\delta}$ [1]、$\{z:\cdots\}$ 形式的「shell-like regions」[5]、记为 $dB_n(\varepsilon)$ 的「spherical shell」[4]，以及在 $\mathbb{C}^2$ 中「可视化为单位球面的一个薄管状邻域」的 shell $U$ [3]。

名称相近，性质却几乎相反——这正是本文要澄清的区分点。需要预先说明：**"annulus/spherical shell" 一词在流体力学与地球物理中另有所指**（两同心球面之间的流体域，如地幔对流、外核对流、旋转球壳热对流）[11][12][13][14][15]，与复分析无关。二者只是术语碰撞，不应混用。下文只在复分析意义下讨论。

## 二、$n=1$：圆环是全纯域

在一维复分析中，圆环 $A$ 是最典型的非单连通区域，但它仍然是**全纯域**：[[全纯域定理三条]] 中的定理 (i) 指出，$n=1$ 时每个区域都是全纯域，圆环自然是其中一例。函数 $1/z$（当 $a=0$ 退化为去心圆盘时可取 $1/z$；一般圆环中可取洛朗级数给出的、在内边界外发散的函数）在 $A$ 上全纯而不可能跨越内边界圆延拓到孔洞里。参见 [[洛朗级数]]、[[解析延拓]] 与 [[恒等原理]]。

因此在一维情形下，"孔洞"是**真实的**：全纯函数能够"看见"它，孔洞构成延拓的障碍。与 [[伪凸域]] 的说法一致，$A$ 也是伪凸的；这与 [[冈洁主定理全纯域等价于伪凸域]] 中"全纯域 $\iff$ 伪凸域"的等价刻画相容。

## 三、$n\ge2$：球壳不是全纯域

在 $\mathbb{C}^n$（$n\ge2$）中，同一公式给出的球壳**不是全纯域**。已有 wiki 页面 [[例4圆环A非全纯域]] 记录了这一事实：圆环 $A$ 上的任一全纯函数都可以外扩，故 $A$ 不是全纯域。随之由 [[例5圆环非全纯域因而非伪凸域]] 得到，$A$ 也不是 [[伪凸域]]。这里的直觉反差值得强调：球壳的两片边界（两个球面）各自作为球体的边界是**严格伪凸**的，但由它们夹出的**区域本身并不伪凸**——伪凸性是区域的整体性质，不能被边界分支的局部凸性所替代。

球壳上的外扩现象是 [[多复变函数]] 中著名的 **Hartogs 现象**（Hartogs phenomenon）的特例，其一般形式即 **Hartogs 延拓定理**：若 $D\subset\mathbb{C}^n$（$n\ge2$）为区域，$K\subset D$ 紧致且 $D\setminus K$ 连通，则 $D\setminus K$ 上的全纯函数必可延拓到 $D$ 上。取 $D$ 为球 $\|z\|<R$、$K$ 为闭球 $\|z\|\le r$，则 $D\setminus K$ 正是球壳 $\{r<\|z\|<R\}$，其包络（envelope of holomorphy）就是整个球 $\|z\|<R$ [1][2][5]。

来源还给出该现象的若干推广与等价视角：

- **Morse 理论的证明途径**：Hartogs 延拓定理可以推广到"集族式"的区域，延拓由 $\mathrm{Shell}_{r,r+\delta}$ 型区域逐步进行 [1]。
- **(n−1)-complete 复空间**：在 $\mathbb{C}$ 之外的复空间上，延拓定理对 $\{z:\cdots\}$ 形式的壳状区域成立，其证明用对 $c$ 的递减归纳 [5]。
- **非分离 Riemann 域**：球壳可视为 $\mathbb{C}^2$ 中单位球面的薄管状邻域，Hartogs 现象是其上的核心问题 [3]。
- **球壳作为障碍**：球壳可以反过来作为全纯映射延拓的障碍，其包络与严格伪凸域的关系是核心工具 [2][4]。

## 四、Reinhardt 域视角：为什么球壳"不可见"

球壳 $\{r<\|z\|<R\}$ 是 [[多复变函数]] 中 **Reinhardt 域**的典型例子：它对每个变量的旋转 $z_j\mapsto e^{i\theta_j}z_j$ 不变，且中心可取为原点 $a=0$ [6][7][8][9][10]。Reinhardt 域的优势在于可以把复几何问题化为 $\mathbb{R}^n$ 中的凸性（对数凸性）问题：把 $D$ 映射到 $\log D=\{(\log|z_1|,\dots,\log|z_n|)\}$，则（连通的）Reinhardt 域是全纯域当且仅当其对数像凸。

对球壳而言，条件 $r<\|z\|<R$ 在 $\log$ 坐标下变成"某个凸函数的两条水平线之间"，这是 $\mathbb{R}^n$ 中的一个**壳状（环状）区域**，一般并不凸，因此球壳不是全纯域——这与第三节的结论一致。反过来，**完全 Reinhardt 域**（若 $z\in D$ 且 $|\zeta_j|\le|z_j|$ 则 $\zeta\in D$）总是全纯域；球壳不是完全的（它不包含孔内的点），这也从另一侧解释了它的"非全纯域"性。来源 [6][7] 强调 Reinhardt 域上幂级数的展开（参见 [[多元幂级数]]），[7][8] 则给出中心归一化的约定。

## 五、区分要点小结

| 方面 | $\mathbb{C}$ 中的圆环 $A$ | $\mathbb{C}^n$ 中的球壳（$n\ge2$） |
|---|---|---|
| 拓扑 | $S^1\times(a,b)$ | $S^{2n-1}\times(r,R)$ |
| 是否全纯域 | 是（$n=1$ 时一切区域皆然） | 否（[[例4圆环A非全纯域]]） |
| 是否伪凸 | 是 | 否（[[例5圆环非全纯域因而非伪凸域]]） |
| 延拓行为 | 孔洞是真实障碍（如 $1/z$） | 一切全纯函数延拓到整球（Hartogs 现象） |
| Reinhardt 对数像 | 一维区间，凸 | 多维壳状，非凸 |
| 包络 | $A$ 自身 | 整球 $\{\|z\|<R\}$ [2] |

一句话概括：**"圆环 vs 球壳"的差别不在于公式，而在于维数**；维数 $\ge2$ 时，全纯函数无法探测球壳内部的"洞"。

## 六、与已有 wiki 页面的关联

本主题与库里 [[10-数学指南实用数学手册--11-11423-多复变函数--kj6en2]] 一节直接相关，其例 4、例 5 正是球壳非全纯域、非伪凸域的标准例子（[[例4圆环A非全纯域]]、[[例5圆环非全纯域因而非伪凸域]]）。更一般的框架见 [[全纯域定理三条]]（n=1 每区域皆全纯域；n≥2 存在非全纯域）、[[冈洁主定理全纯域等价于伪凸域]]、[[全纯域定义与例2Cn为全纯域]]、[[全纯域]]、[[伪凸域]]、[[下调和函数]] 与 [[冈洁]]。相关的延拓工具可挂到 [[解析延拓]]、[[恒等原理]]、[[洛朗级数]]、[[魏尔斯特拉斯预备定理]]。

## 七、矛盾、空白与不确定处

1. **来源 [1]–[5] 均为摘要或 OCR 残片**，大量记号残缺（如 "Shell rr+8(RUN)"、"$\mathrm{Rind}(R_p,,c\,82\,r)$"、"$D\subset\mathbb{C}^n$" 的排版丢失），无法据以逐条核对定理的精确假设（例如 $D\setminus K$ 连通性、$(n-1)$-complete 的定义域族）。本文因此主要依赖已有 wiki 页面中的精确定义。
2. **术语混用风险**：1.14.23 节用「圆环」命名 $\mathbb{C}^n$ 中的集合，与 $\mathbb{C}$ 中圆环同名，易造成读者误解；相关疑点已记于 [[11423节例3与例4中变量与命名疑点]]。
3. **来源 [11]–[15] 与主题实质无关**：它们讨论的是旋转球壳中的热对流、地幔对流等流体问题，"spherical annulus/shell" 指的是两同心球面之间的流体域。若不加区分地纳入同一综述，会与复分析的球壳概念混淆；本文仅作术语碰撞的提示 [11][12][13][14][15]。
4. **Reinhardt 域的对数凸判据**在现有来源 [6]–[10]（多为书籍介绍或书评片段）中未见完整陈述，本文中的表述属于标准结论，尚需更确切的教材级来源支撑。
5. 现有 wiki 中**尚无「Hartogs 现象」或「Hartogs 延拓定理」的独立条目**，也没有 "envelope of holomorphy（全纯包络）" 条目，建议补齐。

## 八、建议补充的来源

- F. Hartogs 关于多复变函数延拓的原始论文（1906），Hartogs 现象与 Hartogs 图形的源头。
- L. Hörmander, *An Introduction to Complex Analysis in Several Variables*：Hartogs 延拓定理、全纯域、伪凸性的标准处理。
- R. M. Range, *Holomorphic Functions and Integral Representations in Several Complex Variables*：球壳与全纯包络的积分表示证明。
- S. G. Krantz, *Function Theory of Several Complex Variables*：Reinhardt 域与对数凸性的完整陈述。
- M. Jarnicki, P. Pflug, *First Steps in Several Complex Variables: Reinhardt Domains*（即来源 [10] 所评之书）：Reinhardt 域几何的系统教材 [6][10]。
- 关于 Morse 理论证明 [1]、(n−1)-complete 复空间 [5] 的完整论文原文，以便核对定理的确切条件。

## References

1. [A Morse-theoretical proof of the Hartogs extension theorem](https://link.springer.com/article/10.1007/BF02922095) — link.springer.com
2. [Spherical shells as obstructions for the extension of holomorphic mappings](https://link.springer.com/article/10.1007/BF02934586) — link.springer.com
3. [On the Hartogs-phenomenon and extension of analytic hypersurfaces in non-separated Riemann domains](https://www.tandfonline.com/doi/pdf/10.1080/02781070290013820) — tandfonline.com
4. [Two theorems on extensions of holomorphic mappings](https://publications.ias.edu/sites/default/files/twotheorems.pdf) — publications.ias.edu
5. [The Hartogs extension theorem on (n-1)-complete complex spaces](https://arxiv.org/abs/0704.3216) — arxiv.org
6. [First steps in several complex variables: Reinhardt domains](http://ems.press/content/book-files/19431?nt=1) — ems.press
7. [Several complex variables](https://books.google.com/books?hl=en&lr=&id=4gwDCAAAQBAJ&oi=fnd&pg=PA1&dq=Reinhardt+domain+definition+several+complex+variables&ots=62lahPcNtx&sig=8SUuxmVT5BB1SPYfLElqxTEq-Z8) — books.google.com
8. [Introduction to complex analysis: functions of several variables](https://books.google.com/books?hl=en&lr=&id=h5H4AwAAQBAJ&oi=fnd&pg=PR9&dq=Reinhardt+domain+definition+several+complex+variables&ots=ITcHborMZA&sig=Z94A145utFB1xlrXw1NWWVSd3FE) — books.google.com
9. [Reinhardt Domains](https://www.ime.usp.br/~cordaro/wp-content/uploads/2026/01/Reinhardt_Domains_Vfinal.pdf) — ime.usp.br
10. [M. Jarnicki, P. Pflug: First Steps in Several Complex Variables: Reinhardt Domains. viii+ 359 pages,€ 58.](https://ems.press/doi/pdf/10.4171/EM/225) — ems.press
11. [On the onset of thermal convection in a rotating spherical shell with spatially heterogeneous heat source distribution](https://pubs.aip.org/aip/pof/article/36/12/124104/3323666) — pubs.aip.org
12. [Exact Poincare Constants in n-dimensional Annuli](https://arxiv.org/pdf/2606.04765) — arxiv.org
13. [Linear stability of natural convection in spherical annuli](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/linear-stability-of-natural-convection-in-spherical-annuli/A3BFC7BB2DB973C8F635209FE53496FD) — cambridge.org
14. [Modeling mantle convection in the spherical annulus](https://www.sciencedirect.com/science/article/pii/S0031920108001921) — sciencedirect.com
15. [Chaotic thermal convection in a rapidly rotating spherical shell: consequences for flow in the outer core](https://www.sciencedirect.com/science/article/pii/0031920194900752) — sciencedirect.com
