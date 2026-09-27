---
type: query
title: "Research: 关联勒让德函数（associated Legendre functions）尚无独立页面"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 关联勒让德函数（associated Legendre functions）尚无独立页面

# 关联勒让德函数

**关联勒让德函数**（associated Legendre functions），在文献中常与**关联勒让德多项式**（associated Legendre polynomials）混用同一称谓，是经典勒让德多项式 $P_n(x)$ 带有一个附加整数（或半整数）指标 $m$ 的推广族。它们与 [[贝塞尔函数]]、[[高斯超几何函数]] 同属数学物理中由二阶常微分方程分离变量而生的特殊函数家族，并且在球坐标下求解 Laplace 方程、构造球谐函数（spherical harmonics）时扮演核心角色 [7][8][9][10]。本页为新建页面，用于汇总目前收集到的资料；需注意所收来源多为片段性摘录，尚未给出完整系统化的定义。

## 概述

所收集来源一致把关联勒让德函数置于以下语境中：

- **正交多项式理论**：勒让德多项式与函数被列为特殊函数与正交多项式教材中的独立一章，与 Hermite、Laguerre 等正交多项式并列讨论 [3]。
- **球谐函数的角向部分**：球谐函数是球面 Laplace 算子的特征函数，其角向结构由关联勒让德函数给出 [7]。来源 [6] 明确以「归一化关联勒让德函数 $A(q,t)$」的形式给出球谐函数的显式表示。
- **应用驱动**：关联勒让德多项式与球谐函数是化学、计算机图形学、磁学等多个领域的核心计算工具 [8]，这促使人们为其开发专用的快速变换与数值库 [7][9]。

## 与勒让德多项式的关系

来源 [2] 系统回顾了勒让德多项式 $P_n(x)$ 的起源与主要性质，指出：

- 定义域为 $x \in [-1, 1]$，且相关函数在该区间上「分段连续」（continuous by parts）；
- **正交性**是 $P_n(x)$ 最基本的特征之一，也是许多应用（包括「shifted Legendre polynomials」在无理性证明中的应用）得以展开的基础 [2]。

来源 [3] 将「Legendre Polynomials and Functions」与 Hermite、Laguerre 及其他正交多项式分章处理，说明关联族（带指标 $m$）被视为该经典族的直接延伸。来源 [5] 进一步把勒让德多项式与经典的 Jacobi 多项式联系起来，讨论其正交性、微分性质以及极值/极小化性质 [5]，这为理解关联勒让德函数作为更一般 Jacobi/超几何族特例的地位提供了背景（参见 [[高斯超几何函数]]）。

> **术语提示**：来源在「函数」与「多项式」之间并不严格区分。带指标 $m>0$ 时 $P_n^m(x)$ 含因子 $(1-x^2)^{m/2}$，一般在开区间上并非严格意义的多项式，但文献常沿用「关联勒让德多项式」这一名称 [8][10]。

## 正交性与完备性

正交性是所收来源反复强调的属性：

- [2] 指出 $P_n(x)$ 的正交性是其应用的基础；
- [5] 对两族正交多项式 $\{Q_n\}_{n\ge 2}$、$\{q_n\}_{n\ge 0}$ 讨论正交性、微分与极值/极小化性质，并经由 Jacobi 多项式框架处理 [5]；
- 在球谐语境下，关联勒让德函数构成球面上的完备正交集，从而保证特征函数展开的收敛性 [7]（可与 [[完备规范正交系]]、[[傅里叶方法]] 对照，后者是同一「按正交特征函数展开」思想在贝塞尔/圆盘情形下的实现）。

## 与球谐函数的关系

这是所收来源覆盖最密集的部分：

- 球谐函数是球面 Laplace 算子的**特征函数**，其显式表达需要「对关联勒让德函数的描述」[7]。
- [6] 通过一个引理确定某个函数为球谐函数，并给出「归一化关联勒让德函数 $A(q,t)$」的显式表示 [6]。
- [10] 把「关联勒让德多项式」「普通球谐函数（ordinary spherical harmonic）」与「修正球谐函数（modified spherical harmonic）」联系起来，指出它们通过简单的变换因子相互关联 [10]。
- [7] 以「球谐函数的快速变换」为动机，强调高效算法对关联勒让德函数的依赖 [7]。

## 归一化约定：一个关键难点

来源 [9] 给出最直接的警告：**关联勒让德函数与球谐函数都存在多种互不相同的约定**（"Many different conventions exist for both the associated Legendre and spherical harmonic functions"）。该来源（SHTools）因此专门为「实归一化」与「复 4π-归一化」两套函数列出全部必要定义 [9]。

来源 [10] 也提到，关联勒让德多项式、普通球谐函数与修正球谐函数之间由「简单的因子」相联系，但这些因子在不同文献中的取法并不统一 [10]。

> **矛盾/风险点**：由于归一化（Condon–Shortley 相位、$\sqrt{(2-\delta_{m0})(2n+1)(n-m)!/(n+m)!}$ 之类因子、实/复形式）差异，直接比较不同来源给出的 $P_n^m$ 或球谐函数值可能得到相差常数因子的结果。使用时必须核对所采用的约定 [9]。

## 数值计算与实现

- [8] 面向化学应用综述了关联勒让德多项式与球谐函数的计算方法，指出其应用远超化学，涵盖计算机图形学与磁学 [8]。
- [7] 提供球谐函数的快速变换算法 [7]。
- [9] 的 SHTools 是一个可直接使用的工具集，内含实/复两种归一化下的定义与计算例程 [9]。

## 相关但不同的对象

- **Müntz–Legendre 多项式**：来源 [1] 与 [4] 讨论 Müntz 系统与正交 Müntz–Legendre 多项式。[1] 指出该类函数关于 Lebesgue 测度的正交性将在其推论 2.3 中证明 [1]；[4] 分析 Müntz–Legendre 多项式与经典 Legendre 多项式、Jacobi 多项式的联系，并给出逼近性质与一条正交性引理（Lemma 3.3）[4]。**注意**：Müntz–Legendre 族是对指数集合做 Müntz 型限制所生成的正交族，与「关联勒让德函数」不是同一对象，切勿混淆。
- **Jacobi 多项式**：[5] 经由 Jacobi 多项式统一处理勒让德族及其变体 [5]，提示关联勒让德函数可作为更一般超几何族（参见 [[高斯超几何微分方程]] 与 [[Pochhammer符号]]）的特例来理解。

## 缺口与待补内容

所收来源未直接给出（因此本页暂缺）以下内容，建议后续查阅权威教材补全：

1. **显式定义式**：如 $P_n^m(x) = (1-x^2)^{m/2}\,\dfrac{d^m}{dx^m}P_n(x)$ 及其 Rodrigues 型公式；当前来源仅给出称谓与性质 [2][3]。
2. **所满足的微分方程**：关联勒让德方程及其奇点结构，是否可归入 [[奇异微分方程]] / [[正则奇点]] 的 Frobenius 框架（参见 [[Frobenius幂级数解法]]）。
3. **$m$ 与 $n$ 的取值约定**：$|m| \le n$、$m$ 为负或半整数时如何延拓。
4. **递推关系**：用于数值计算的稳定递推。
5. **与合流/高斯超几何函数的具体对应**：$P_n^m$ 与 ${}_2F_1$ 的转换关系 [3][5]。

## 建议补充来源

- 经典特殊函数手册（如 Abramowitz & Stegun、DLMF）中的 "Associated Legendre Functions" 章节——用于确定定义、归一化与递推关系。
- 球谐函数专著（例如与 [6] 同源的教材）——用于确认 $A(q,t)$ 归一化与 Condon–Shortley 相位的对应 [6]。
- SHTools 的文档与技术说明——用于实/复两种归一化的完整对照 [9]。
- 一篇系统性的球谐函数计算综述（例如 [8] 的全文）——用于数值稳定性比较 [8]。

## 相关内容

- [[高斯超几何函数]]、[[高斯超几何微分方程]]、[[Pochhammer符号]]：关联勒让德函数所属的超几何框架。
- [[贝塞尔函数]]、[[诺伊曼函数]]：同源于分离变量的另一特殊函数族（圆柱坐标）。
- [[拉普拉斯]]：Laplace 方程及其在球坐标下的分离变量是关联勒让德函数的主要出处。
- [[完备规范正交系]]、[[傅里叶方法]]：正交展开这一共同方法的其他实例。
- [[奇异微分方程]]、[[正则奇点]]、[[Frobenius幂级数解法]]：关联勒让德方程的解法背景。

## References

1. [Müntz systems and orthogonal Müntz-Legendre polynomials](https://www.ams.org/tran/1994-342-02/S0002-9947-1994-1227091-4/) — ams.org
2. [Lecture notes on Legendre polynomials: their origin and main properties](https://arxiv.org/abs/2210.10942) — arxiv.org
3. [Special functions and orthogonal polynomials](https://books.google.com/books?hl=en&lr=&id=r3Zj__Ag7LwC&oi=fnd&pg=PA3&dq=Legendre+polynomials+associated+Legendre+functions+orthogonality+L2(-1,1)&ots=396Eqq3CP6&sig=xQJz0RHOYbsFvswv1zQUdJmtgGg) — books.google.com
4. [Müntz Legendre polynomials: Approximation properties and applications](https://www.ams.org/mcom/2025-94-353/S0025-5718-2024-03987-X/S0025-5718-2024-03987-X.pdf) — ams.org
5. [Integral of Legendre polynomials and its properties](https://mcs.qut.ac.ir/article_729111.html) — mcs.qut.ac.ir
6. [Spherical harmonics](https://books.google.com/books?hl=en&lr=&id=9hx6CwAAQBAJ&oi=fnd&pg=PA1&dq=spherical+harmonics+normalized+associated+Legendre+polynomial+definition&ots=J9_Be12fb0&sig=bJxBXuwT10DChIaS0LioGnzM1VE) — books.google.com
7. [A fast transform for spherical harmonics](https://link.springer.com/article/10.1007/BF01261607) — link.springer.com
8. [Associated Legendre polynomials and spherical harmonics computation for chemistry applications](https://arxiv.org/abs/1410.1748) — arxiv.org
9. [SHTools: Tools for working with spherical harmonics](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2018GC007529) — agupubs.onlinelibrary.wiley.com
10. [Associated Legendre polynomials, ordinary and modified spherical harmonics](https://www.sciencedirect.com/science/article/pii/0010465573900659) — sciencedirect.com

## Related
- [[queries/research-勒让德多项式与关联勒让德函数-2026-09-27-091938-research-318]]
