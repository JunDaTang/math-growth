---
type: query
title: "Research: 正切与余切在复平面上的极点结构（亚纯函数）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 正切与余切在复平面上的极点结构（亚纯函数）

# 正切与余切在复平面上的极点结构（亚纯函数）

## 概述

[[正切与余切]] 作为两个全纯函数之商，在有限复平面内并非处处有定义，而是被一列孤立奇点打断。这些奇点全部是**单极点（simple pole）**，且只向无穷远点累积，因此 tan z 与 cot z 都是**亚纯函数（meromorphic function）** [11]。本页综合 Mittag-Leffler 展开定理的部分分式视角，梳理这两个函数的极点位置、阶与留数，并说明它们如何统一于 [[余切部分分式分解]] 与 [[欧拉正弦乘积公式]] 的框架之中。

## 复平面上的定义

复值正切与余切沿用与实值相同的商式：

$$\tan z = \frac{\sin z}{\cos z}, \qquad \cot z = \frac{\cos z}{\sin z}$$

借 [[欧拉公式]] 消去 sin、cos 后，可写成纯指数形式（Euler 公式的直接推论）[11]：

$$\tan z = -i\,\frac{e^{2iz}-1}{e^{2iz}+1}, \qquad \cot z = i\,\frac{e^{2iz}+1}{e^{2iz}-1}$$

百度百科条目亦给出复变分析中余切的标准型 $\cot(z)=i(e^{2iz}+1)/(e^{2iz}-1)$ [10]。这属于 [[三角函数的指数表示]] 的具体实例。

由于 [[毕达哥拉斯三角恒等式]] $\cos^2 z + \sin^2 z = 1$ 保证 cos 与 sin 不会同时为零，商在**一切有限点**处总是有限的；发散只可能来自分母的零点 [11]。

## 亚纯性：极点只向无穷远累积

极点的位置可由 $e^{2iz}$ 的取值读出：

- $\cot z$ 的分母 $e^{2iz}-1=0 \iff e^{2iz}=1$。由 [[复指数函数的周期性]]，这当且仅当 $2iz = 2\pi i k$，即

$$z = k\pi, \quad k \in \mathbb{Z}$$

- $\tan z$ 的分母 $e^{2iz}+1=0 \iff e^{2iz}=-1$，即

$$z = \frac{\pi}{2} + k\pi, \quad k \in \mathbb{Z}$$

这些点构成为等差列，仅以 $z=\infty$ 为聚点。既然 cot 与 tan "在除这些极点外的所有有限点全纯，而极点只累积到 $\infty$"，二者即为亚纯函数 [11]。这与 [[正切与余切的零点与极点皆为单的]] 一致，也修正、补充了 [[正切余切的零点与极点]] 在实数轴上的描述。

## 极点的阶与留数

每个极点都是**一阶（单）极点**，因为分母在相应点只有单零点 [11]。留数可由"单极点留数 = 分子 / 分母导数"求得：

| 函数 | 极点 | 阶 | 留数 |
|---|---|---|---|
| $\cot z$ | $z = k\pi$ | 1 | $+1$ |
| $\tan z$ | $z = \dfrac{\pi}{2}+k\pi$ | 1 | $-1$ |

留数对一切 $k$ 相同，正是余切部分分式展开中"每对极点系数相同"的来源 [2]。源 [2][13] 在讨论 Mittag-Leffler 展开与 Laurent 展开时，均以"先定极点、再求留数"为流程。

## Mittag-Leffler 展开

### 一般定理

若 $f(z)$ 是亚纯函数，仅在 $z_1, z_2, z_3, \dots$（满足 $0<|z_1|\le|z_2|\le\cdots$）拥有一阶极点，对应留数为 $r_1, r_2, r_3, \dots$，则 [2]

$$f(z) = f(0) + \sum_{n=1}^{\infty}\left( \frac{r_n}{z-z_n} + \frac{r_n}{z_n} \right)$$

这就是 **Mittag-Leffler（M-L）展开**。它断言：可以**任意指定**极点和主部，构造出在整个复平面上亚纯的函数，并给出描写全部这类函数的显式形式；但一般形式"主要具理论意义，因为不易在具体情形中应用"——通常需要对函数附加额外假设（例如在半径递增的圆周序列 $C(0;r_n)$ 上一致有界）才能得到有用的具体公式 [4]。

### 余切的欧拉展开

在具体函数上，M-L 展开最经典的结果正是余切。欧拉在 1748 年《Introductio in analysin introductorium / Introductio in analysin infinitorum》中即已给出 [2]：

$$\cot z = \frac{1}{z} + \sum_{n=1}^{\infty}\left( \frac{1}{z-n\pi} + \frac{1}{z+n\pi} \right)$$

这正是 [[余切部分分式分解]] 的核心公式，也是 [[欧拉正弦乘积公式]] 取对数导数后的直接结果，并与 [[巴塞尔问题与欧拉zeta公式]] 同源。其推导可在 Whittaker & Watson 的 *A Course of Modern Analysis*（第 4 版，1958，pp. 134ff.）中查到 [2]；[4] 亦引用经典文献将 cot 的部分分式作为该定理的应用范例。

### 正切与 cot²、csc² 的展开

- **正切与 coth**：源 [1] 明确说明用 Mittag-Leffler 展开定理得到 $\tan z$ 与 $\coth z$ 的部分分式展开。由于 $\tan z$ 的极点位于 $\pi/2 + k\pi$、留数全为 $-1$，其展开结构与余切仅差一次平移，呼应 [[余切全部性质可由正切经平移得到]]。
- **余切平方**：$\cot^2 z$ 在同样极点处是**二阶**极点，其展开并非简单地把 $\cot z$ 级数逐项平方。源 [3] 指出该展开与余割平方的关系应写作

$$\cot^2 z = \csc^2 z - 1, \qquad \csc^2 z = \frac{1}{\sin^2 z}$$

- **$1/\sin^r z$ 族**：[4] 指出对每个 $r\in\mathbb{N}$，$1/\sin^r z$ 都是整个复平面上的亚纯函数，除孤立极点外处处解析，可作为 M-L 型部分分式推导的对象。

## 与实数域图像的联系

把复平面上这些单极点沿实轴"切片"，得到的正是初等教材中正切、余切图像的**竖直渐近线** [6][12][15]：

- $\cot x$ 的渐近线在 $x=k\pi$，零点位于渐近线中点 $x=\dfrac{\pi}{2}+k\pi$，周期为 $\pi$ [6][12]。
- $\tan x$ 的渐近线在 $x=\dfrac{\pi}{2}+k\pi$，零点在 $x=k\pi$ [12]。
- 复平面视角下，极点是三维复图中"尖峰"状的孤立奇点，其自变量以颜色编码，[2] 的演示即以此可视化 $\cot$、$\Gamma$ 等函数的极点。

## 历史脉络

- 1707 年，[[棣莫弗]] 在《分析杂论》中推导复数形式的余切展开式，为后续级数研究奠基（据 [10]）。
- 1748 年，欧拉在《无穷小分析引论》中给出 $\cot z$ 的部分分式展开，并系统化三角函数的积分表达式 [2][10]。这与 [[三角学的历史发展]] 以及 [[韦达]]、[[雷乔蒙塔努斯]]、[[图西]] 所代表的早期三角学传统一脉相承。
- 1876 年，Mittag-Leffler 发表关于有理型函数解析表示的开创性论文，确立了以极点与主部刻画亚纯函数的定理 [2][4]。

## 与既有知识的关系

- [[正切与余切]]、[[三角函数的零点]] —— 给出定义与实轴零点；
- [[正切余切的零点与极点]]、[[正切与余切的零点与极点皆为单的]] —— 本页的极点结构是其在复域上的完整版本；
- [[余切部分分式分解]]、[[欧拉正弦乘积公式]] —— 余切展开的两种等价推导途径；
- [[三角函数的指数表示]]、[[复指数函数的周期性]]、[[欧拉公式]] —— 提供指数型定义与极点定位的工具；
- [[棣莫弗]] —— 复数余切展开的早期贡献者。

## 矛盾、空白与待核问题

1. **cot² 展开的表述**：源 [3] 以论坛问答形式出现，措辞含混（"缺了乘以 cos² 的项……故 $\cot^2=\csc^2-1$"）。应以恒等式 $\cot^2 z = \csc^2 z - 1$ 为准，但其**逐项部分分式**的系数需另找权威来源核对。
2. **$\tan z$、$\coth z$ 的显式系数**：源 [1] 只声明"用 M-L 定理得到"，未给出各项表达式；本页据极点与留数推得的结构（极点 $\pi/2+k\pi$、留数 $-1$）应与之一致，但仍缺一手公式。
3. **定理的适用条件**：[2][4] 均强调一般 M-L 定理"偏理论"，须附加一致有界等条件才便于计算，本页未展开该条件的完整表述。
4. **史料细节**：[10] 关于棣莫弗 1707 年复数余切展开式的说法，与主流数学史著作（如 [[三角学的历史发展]] 相关来源）可能存在出入，宜再核。

## 建议补充的来源

- E. T. Whittaker & G. N. Watson, *A Course of Modern Analysis*, 4th ed., Cambridge University Press, 1958, pp. 134ff. —— 余切部分分式与 M-L 展开的经典处理 [2]。
- G. Mittag-Leffler, "En metod att analytisk framställa en funktion af rationel karaktär…", *Öfversigt Kongl. Vetenskaps-Akademiens Förhandlinger*, 33 (1876), pp. 3–16 —— 定理原始文献 [2]。
- R. Nevanlinna & V. Paatero, *Funktioteoria*, Otava, Helsinki, 1963 —— 复正切/余切定义的参考文献 [11]。
- 《数学指南——实用数学手册》0.2.9 正切与余切（见 [[10-数学指南实用数学手册--9-029-正切与余切--5y4yea]]）—— 可作为符号与零点/极点约定的本地化基准。
- 一篇系统讨论 $\tan z$ 与 $\coth z$ M-L 展开系数的论文或教材章节，用于补全第 2 项空白。

## 来源

[1] *Partial Fraction Expansion of Meromorphic Maps*（researchgate.net）—— 用 Mittag-Leffler 展开定理得到 $\tan z$ 与 $\coth z$ 的部分分式展开。
[2] *Mittag-Leffler Expansions of Meromorphic Functions*（wolframcloud.com）—— M-L 展开一般式、欧拉 1748 余切展开、Whittaker & Watson 与 Mittag-Leffler 1876 引用、复平面极点 3D 可视化。
[3] *Mittag-Leffler fractions for $\cot^2 z$ and $\frac{1}{\sin^2\pi z}$*（math.stackexchange.com）—— $\cot^2 z = \csc^2 z - 1$ 的关系说明。
[4] *Partial Fraction Decomposition of Some Meromorphic Functions*（ac.inf.elte.hu）—— M-L 定理的陈述、一致有界条件、$1/\sin^r z$ 的亚纯性、cot 部分分式推导。
[5] Chegg 习题：用 Mittag-Leffler 部分分式展开定理证明 $\cot z$ 的展开（chegg.com）。
[6] 余切（百度百科）—— 实数域定义域、渐近线、零点，及复数域标准型 $\cot(z)=i(e^{2iz}+1)/(e^{2iz}-1)$。
[7] 余切（百度百科，baike.baidu.com）。
[8] 余切（百度百科，baike.baidu.com）。
[9] 余切（百度百科，baike.baidu.hk）。
[10] 余切函数（百度百科）—— 复域标准型、应用与历史（含棣莫弗、欧拉条目）。
[11] *complex tangent and cotangent*（planetmath.org）—— 复正切/余切定义、单极点论证、亚纯性、参考 Nevanlinna & Paatero。
[12] *Graphs of Tangent and Cotangent Functions*（pearson.com）—— 渐近线与零点的实轴位置。
[13] *Cotangent Function Expansion Analysis*（scribd.com）—— 用 Laurent 展开确定极点阶与留数。
[14] *Zeros and poles*（Wikipedia）—— 极点与亚纯函数的一般定义。
[15] *Mastering Graphing of Tangent & Cotangent Functions*（youtube.com）—— 渐近线来自分母零点、周期为 $\pi$ 的图像解释。

## References

1. [Partial Fraction Expansion of Meromorphic Maps](https://www.researchgate.net/publication/362996100_Partial_Fraction_Expansion_of_Meromorphic_Maps) — researchgate.net
2. [Mittag-Leffler Expansions of Meromorphic Functions](https://www.wolframcloud.com/obj/947075ad-6ea3-4235-aa96-22235b1f7809?src=CloudBasicCopiedContent) — wolframcloud.com
3. [Mittag-Leffler fractions for $\cot^2z$ and $\frac{1}{\sin^2\pi z}](https://math.stackexchange.com/questions/3575236/mittag-leffler-fractions-for-cot2z-and-frac1-sin2-pi-z) — math.stackexchange.com
4. [PARTIAL FRACTION DECOMPOSITION OF SOME ...](https://ac.inf.elte.hu/Vol_038_2012/doi/093_38.pdf) — ac.inf.elte.hu
5. [Solved 3. Using the Mittag Leffler Partial Fraction](https://www.chegg.com/homework-help/questions-and-answers/3-using-mittag-leffler-partial-fraction-expansion-theorem-22-2-2z-prove-following-cot-z-q37704886) — chegg.com
6. [余切_百度百科](https://baike.baidu.hk/item/%E4%BD%99%E5%88%87/9601625) — baike.baidu.hk
7. [余切_百度百科](https://baike.baidu.com/item/%E4%BD%99%E5%88%87/9601625) — baike.baidu.com
8. [余切_百度百科](https://baike.baidu.com/item/%E4%BD%99%E5%88%87/0) — baike.baidu.com
9. [余切_百度百科](https://baike.baidu.hk/item/%E4%BD%99%E5%88%87/0) — baike.baidu.hk
10. [余切函数_百度百科](https://baike.baidu.com/item/%E4%BD%99%E5%88%87%E5%87%BD%E6%95%B0/10798631) — baike.baidu.com
11. [complex tangent and cotangent](https://planetmath.org/complextangentandcotangent) — planetmath.org
12. [Graphs of Tangent and Cotangent Functions - Pearson](https://www.pearson.com/channels/trigonometry/learn/patrick/04-graphing-trigonometric-functions/graphs-of-tangent-and-cotangent-functions) — pearson.com
13. [Cotangent Function Expansion Analysis | PDF](https://www.scribd.com/document/862705052/Practical-15-copy-complex-analysis) — scribd.com
14. [Zeros and poles - Wikipedia](https://en.wikipedia.org/wiki/Zeros_and_poles) — en.wikipedia.org
15. [Mastering Graphing of Tangent & Cotangent Functions - [2-21-15]](https://www.youtube.com/watch?v=VyiKxdz4BmU) — youtube.com
