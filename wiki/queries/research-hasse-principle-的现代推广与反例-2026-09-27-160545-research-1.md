---
type: query
title: "Research: Hasse principle 的现代推广与反例"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: Hasse principle 的现代推广与反例

# Hasse principle 的现代推广与反例

## 概述

**Hasse principle**（局部–整体原则，local–global principle）指：一个定义在整体域（如 $\mathbb{Q}$ 或函数域）上的代数簇，若在它的**所有**完备化（包括实位、复位与各 $p$-进位）上都有有理点，则它本身也有有理点。该原则对二次型成立（Hasse–Minkowski 定理），但对三次及更高次的对象一般不成立。

本页汇总的资料来源显示，围绕 Hasse principle 的现代研究有两条主线：

1. **反例的构造与扩展**：从 Selmer 的单个三次曲线反例，发展到三次曲面上的无穷多反例，直至证明这类反例在非奇异三次曲面的 moduli scheme 中 Zariski 稠密 [1][4][5]。
2. **障碍理论的建立与推广**：用 **Brauer–Manin 障碍**（Manin obstruction）来解释局部–整体原则的失败，并将其推广到积分情形、函数域、嵌入问题乃至动力系统类比 [3][6][7][8][9][10]。

---

## 经典反例：Selmer 三次曲线

最常被引用的入门级反例是 Selmer 的三次曲线

$$3x^3 + 4y^3 + 5z^3 = 0,$$

它在 $\mathbb{Q}$ 的所有完备化中都有非平凡解，却没有非平凡的整数（或有理）解，因此构成 Hasse principle 的失败实例 [11][13]。Keith Conrad 的讲义给出了具体的局部解构造：在 $\mathbb{R}$ 中有解 $(\sqrt[3]{5/3},\,0,\,-1)$；在 $\mathbb{Q}_3$ 中有解 $(0,\,y,\,-1)$，其中 $y^3 = 5/4$ [12]。"该方程在每个 $\mathbb{Q}_p$ 与 $\mathbb{R}$ 中均可解"这一点在多份讲义与习题中被反复作为练习或引理给出 [14][15]。

需要注意的**记号不一致**：部分材料把反例写作射影三次曲线 $3x^3+4y^3+5z^3=0$ [11][13][15]，另一些材料讨论仿射形式 $3x^3 + 4y^3 = 5$ [14]。二者在齐次化后是同一对象的两种表述，但在讨论"整数解"与"有理点"时含义不同，引用时应明确所处的是仿射还是射影框架。此外，有些资料只笼统地说"三次（或更高次）型"破坏 Hasse principle [13]，未区分**型（form）**与**簇（variety）**——这是后续文献中反例类型多样化的根源。

Selmer 反例的意义在于：它表明 Hasse–Minkowski 式的局部–整体原则**不能**从二次型推广到三次型。对亏格 0 的曲线（圆锥曲线）Hasse principle 仍然成立，而 Selmer 曲线是亏格 1 的平面三次曲线，恰好处在原则开始失效的边界。

---

## 三次曲面上的反例与 Zariski 稠密性

较新的工作把反例从曲线推进到**曲面**：

- **Swinnerton-Dyer** 证明了在 $\mathbb{Q}$ 上存在违反 Hasse principle 的光滑三次曲面 $V \subset \mathbb{P}^3$；这一存在性结论常被用作构造其他反例（例如亏格一曲线族）的出发点 [5]。
- **Mordell** 曾给出使 Hasse principle 失败的三次曲面的构造，后续文献在此基础上构造出"更多"这类曲面 [4]。
- 更进一步的结果表明，违反 Hasse principle 的三次曲面在**非奇异三次曲面的 moduli scheme 中是 Zariski 稠密的** [1]。也就是说，反例并非孤立的病态特例，而是在参数空间的意义下"随处可见"。

这条线索的**论述缺口**在于：现有资料来源只提供了标题与摘要级别的信息 [1][4][5]，没有给出稠密性定理的证明思路、所依赖的 Brauer 群计算，也没有说明这些构造与下面将要讨论的 Brauer–Manin 障碍之间的精确对应关系（三次曲面上的失败是否**总是**由 Brauer–Manin 障碍解释，仍是一个需要核对的问题）。

---

## 从反例到障碍理论：Brauer–Manin 障碍

### Manin 障碍的一般框架

**Manin obstruction**（更完整地称为 Brauer–Manin obstruction）是目前解释局部–整体原则失败的主流工具 [6][8]。其基本思想是：把各处的局部点集合嵌入到一个 adelic 空间，再用簇上的 Azumaya 代数（Brauer 群元素）定义一个配对；若某个 Brauer 类在该 adelic 空间上的取值不满足整体约束，就能"排除"整体有理点的存在，即使所有局部点都存在。

对**阿贝尔簇**而言，Manin 障碍恰好就是 **Tate–Shafarevich 群** $\mathrm{Sha}$ 的对偶，并且在（如 $\mathrm{Sha}$ 有限性等）适当假设下**完全**解释了局部–整体原则的失败 [6]。这是障碍理论中最清晰、最经典的一类结果。

### 函数域上的常曲线与"唯一障碍"

在整体函数域上的**常曲线**情形，有结果断言：当曲线 $D$ 的亏格小于 $C$ 的亏格时，Brauer–Manin 是**弱逼近与 Hasse principle 的唯一障碍** [7]。这类"唯一障碍"型定理是障碍理论追求的典范形式，但它的适用范围受亏格条件严格限制。

### 弱逼近与嵌入问题

除 Hasse principle 本身外，Brauer–Manin 障碍还被用于研究**弱逼近**（weak approximation）的失效 [7]，并被类推到**嵌入问题**（embedding problems）在整体域上的局部–整体原则 [9]。这说明障碍理论已经从"有理点是否存在"的判定工具，扩展为处理更一般的局部–整体现象的框架。

---

## 现代推广

### 积分 Hasse principle

经典 Hasse principle 关注**有理点**。若改问**整点**是否存在，就得到**积分 Hasse principle**。资料的来源 [3] 研究了仿射对角三次曲面的**积分 Brauer–Manin 障碍**，并用它构造出了积分 Hasse principle 的**首批反例** [3]。这是把障碍理论从射影情形移植到仿射/积分情形的代表性进展，也提示"局部–整体"问题必须明确所讨论的是哪一类点（有理点、整点、还是 S-整点）。

### 动力系统的 Brauer–Manin 类比

另一类推广是**动力系统的局部–整体原则**：资料来源 [10] 描述了一个针对"交集"的局部–整体原则，并把它视为 Brauer–Manin 障碍的**动力类比**（dynamical analog）[10]。这一方向把算术几何中的障碍思想移植到动力系统（如态射的轨道、周期点）的语言中，是"现代推广"中最具跨领域色彩的一支。

### 理论谱系小结

| 层次 | 对象 | 是否有 Hasse principle | 主要解释工具 |
|---|---|---|---|
| 二次型 | 二次形式 | 成立（Hasse–Minkowski） | — |
| 亏格 0 曲线 | 圆锥曲线 | 成立 | — |
| 亏格 1 三次曲线 | Selmer 曲线 $3x^3+4y^3+5z^3=0$ | 失败 [11][12][13] | 具体的局部解构造 |
| 三次曲面 | $\mathbb{Q}$ 上的光滑三次曲面 | 可失败，且在 moduli 中 Zariski 稠密 [1][5] | Brauer–Manin 障碍 |
| 阿贝尔簇 | 阿贝尔簇 | 可失败 | Manin 障碍 = Tate–Shafarevich 群 [6] |
| 仿射曲面 | 仿射对角三次曲面 | 积分版本可失败 [3] | 积分 Brauer–Manin 障碍 |
| 动力系统 | 态射的轨道/交集 | 类比框架 [10] | 动力 Brauer–Manin 障碍 |

---

## 矛盾、空白与不确定之处

1. **反例的表述不统一**：Selmer 例子在不同资料中分别写作 $3x^3+4y^3+5z^3=0$ 与 $3x^3+4y^3=5$ [11][13][14][15]，射影与仿射框架混用，引用时需谨慎。
2. **"完全解释"的条件未明**：来源 [6] 称 Manin 障碍"完全解释"阿贝尔簇上局部–整体原则的失败，但这一断言依赖 $\mathrm{Sha}$ 有限性等未在本批资料中展开的假设，需回溯原文核实。
3. **反例与障碍的对应关系缺失**：来源 [1][4][5] 只给出稠密性与构造性结论，未说明这些三次曲面反例是否**全部**由 Brauer–Manin 障碍解释。是否存在"超越 Brauer–Manin 障碍"的失败，是本主题中最关键的开放问题之一，本批资料未提供答案。
4. **可用信息粒度有限**：这批来源多为标题、摘要与讲义片段（尤其是 [1][3][4][5][7][9]），缺少证明细节、参数条件与显式数值例子。
5. **术语层次混淆**："Hasse principle 失败"有时指曲线，有时指曲面，有时指整点问题 [3]，需要按语境区分。

---

## 建议补充的来源

为补齐上述空白，建议检索以下方向的资料：

- Colliot-Thélène 关于 Brauer–Manin 障碍与有理点的综述性讲义（用于厘清"是否唯一障碍"的现状）。
- Skorobogatov 的专著 *Torsors and Rational Points*（Manin 障碍的系统处理）。
- Poonen, *Rational Points on Varieties*（局部–整体原则与障碍的教科书式叙述）。
- Bryden / Kollár 等关于三次曲面族与稠密性定理的原始论文全文（支撑来源 [1]）。
- 关于 **$\mathrm{Sha}$ 有限性**与 Tate–Shafarevich 群的标准参考文献（支撑来源 [6] 的"完全解释"表述）。
- 动力系统算术的最新论文（支撑来源 [10] 的动力 Brauer–Manin 障碍）。
- 函数域上弱逼近的专门文献（支撑来源 [7] 的亏格条件）。
- 积分有理点与积分 Hasse principle 的综述（支撑来源 [3]）。

---

## 与现有 wiki 的关联

现有 wiki 的页面集中在概率论与数理统计方向（如 [[数学指南-实用数学手册]]、[[数理统计]]、[[随机过程]] 等），与本主题（算术几何、代数数论）**没有直接重叠**，因此本页暂未建立跨页 wikilink。若后续围绕本主题继续积累资料，建议新建以下页面以承接链接：实体页 `entities/Selmer`、`entities/Swinnerton-Dyer`、`entities/Mordell`、`entities/Manin`，概念页 `concepts/Hasse principle`、`concepts/Brauer-Manin 障碍`、`concepts/Tate-Shafarevich 群`、`concepts/积分 Hasse principle`、`concepts/弱逼近`，以及来源页 `sources/` 下对应各条目的独立页面。

## References

1. [Cubic surfaces violating the Hasse principle are Zariski dense in the ...](https://www.sciencedirect.com/science/article/pii/S0001870815001565) — sciencedirect.com
3. [Cubic surfaces failing the integral Hasse principle - arXiv](https://arxiv.org/html/2311.10008v2) — arxiv.org
4. [More cubic surfaces violating the Hasse principle - EuDML](https://eudml.org/doc/219781) — eudml.org
5. [[PDF] an explicit algebraic family of genus-one curves violating the ...](https://math.mit.edu/~poonen/papers/cubics.pdf) — math.mit.edu
6. [Manin obstruction - Wikipedia](https://en.wikipedia.org/wiki/Manin_obstruction) — en.wikipedia.org
7. [The Brauer–Manin obstruction for constant curves over global function ...](https://www.numdam.org/articles/10.5802/aif.3473/) — numdam.org
8. [Local -global problems and the Brauer -Manin obstruction.](https://deepblue.lib.umich.edu/items/07656b2f-2ec1-4d4e-9e91-3eb1aa6bbc9a) — deepblue.lib.umich.edu
9. [The Brauer-Manin obstruction to the local-global principle for the ...](https://ui.adsabs.harvard.edu/abs/arXiv:1602.04998) — ui.adsabs.harvard.edu
10. [On a dynamical Brauer–Manin obstruction - EuDML](https://eudml.org/doc/10874) — eudml.org
11. [Proof of no rational point on Selmer's Curve $3x^3+4y^3+5z^3=0](https://mathoverflow.net/questions/2779/proof-of-no-rational-point-on-selmers-curve-3x34y35z3-0) — mathoverflow.net
12. [[PDF] selmer's example - keith conrad](https://kconrad.math.uconn.edu/blurbs/gradnumthy/selmerexample.pdf) — kconrad.math.uconn.edu
13. [On the equation $3x^3 + 4y^3 + 5z^3 = 0$ - Mathematics Stack Exchange](https://math.stackexchange.com/questions/55119/on-the-equation-3x3-4y3-5z3-0) — math.stackexchange.com
14. [[PDF] Number Theory: Elliptic Curves, Problem Sheet 3](https://www.ma.imperial.ac.uk/~tsg/Index_files/ellcurves3.pdf) — ma.imperial.ac.uk
15. [[PDF] Some exceptions to the local-global principle - Luis Modes](https://luismodes.com/docs/18.782%20Final%20Paper%20%20(Luis%20Modes).pdf) — luismodes.com

## Related
- [[queries/research-局部-整体原理hasse-principle的现代推广与反例-2026-09-27-160545-research-2]]
