---
type: query
title: "Research: 补充拉普拉斯算子本征值的变分表征（Rayleigh 商）"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: 补充拉普拉斯算子本征值的变分表征（Rayleigh 商）

# 拉普拉斯算子本征值的变分表征（Rayleigh 商）

## 概述

拉普拉斯算子（Laplacian，写作 $\Delta$ 或 $\nabla^2$）的本征值问题，即求解

$$\Delta u = \lambda u \quad(\text{或}\ -\Delta u = \lambda u)$$

是谱几何、偏微分方程与数学物理的核心对象。除直接求解微分方程外，本征值与本征函数还可以通过一个**变分原理**来刻画：把算子作用下的二次型与范数之比（即 Rayleigh 商）在适当的函数空间上取极值，其驻点恰为本征函数，极值恰为本征值。这一表征不仅是理论工具，也是有限元、谱方法等数值求解的基础。[2][3][5][7]

本页补充的是该变分表征的系统描述——**Rayleigh 商的极值原理**、**Courant–Fischer 极小极大原理**，以及它在一般区域、闭流形上的推广与空白点。

## Rayleigh 商的定义与基本性质

对作用在实 Hilbert 空间 $H$ 上的自伴算子 $A$，向量 $x\neq 0$ 的 Rayleigh 商定义为

$$R(x) = \frac{\langle Ax, x\rangle}{\langle x, x\rangle}.$$

对本征值问题 $-\Delta u = \lambda u$（例如在区域 $\Omega\subset\mathbb{R}^d$ 上取 Dirichlet 边界条件 $u|_{\partial\Omega}=0$），相应的 Rayleigh 商为

$$R(u) = \frac{\displaystyle\int_\Omega |\nabla u|^2\,dx}{\displaystyle\int_\Omega u^2\,dx},\qquad u \in H^1_0(\Omega),\ u\neq 0,$$

其中分子是 Dirichlet 能量（势能），分母是 $L^2$ 范数的平方。[3][11]

其三条基本性质为：

1. **本征值即驻值**：若 $x$ 是 $A$ 的本征向量，则 $R(x)$ 恰为对应本征值。[5]
2. **极值对应端谱**：当 $x$ 取对应最小/最大本征值的本征向量时，$R(x)$ 取得全局最小/最大值。[7]
3. **变分特征**：$R$ 的极值点即为 $A$ 的本征向量，$R$ 的临界值即本征值。[7]

由此得到第一本征值的最小值刻画——它正是「基态」能量的表述：

$$\lambda_1 = \min_{u\in H^1_0(\Omega),\ u\neq 0} R(u) = \min_{\|u\|_2 = 1}\int_\Omega|\nabla u|^2\,dx.$$

文献 [3] 用物理语言概括为：「第一本征值是势能的最小值，第一本征函数是基态（最低能量态）。」

## Courant–Fischer 极小极大原理

第一本征值的最小值刻画并不能直接给出高阶本征值，因为对 $\lambda_2$ 而言 $R$ 的最小值仍会「坍缩」到 $\lambda_1$。解决办法是对**子空间维度**施加约束，这就是 Courant–Fischer 极小极大原理（亦称 min-max principle、变分原理）。[1][11][12]

设 $H^1_0(\Omega)$ 上的 $-\Delta$ 具有离散谱 $0<\lambda_1\le\lambda_2\le\cdots\to\infty$，则第 $k$ 个 Dirichlet 本征值为

$$\lambda_k = \inf_{\substack{V\subset H^1_0(\Omega)\\ \dim V = k}}\ \sup_{u\in V,\ u\neq 0} R(u).$$

等价地，也可以把 $k$ 维子空间写成与任意 $(k-1)$ 维子空间正交的约束形式（Fischer 形式）。[11][12] 文献 [14] 用有限维矩阵例子（$2\times 2$ 矩阵，最小本征值 $3$、最大本征值 $8$）演示了极小极大公式的运作方式。

该原理的适用范围并不限于欧氏区域上的 Dirichlet 问题：它实际上是**紧自伴算子**（compact Hermitian operators）本征值的通用变分刻画，因而可推广到 Neumann 边界条件、Sturm–Liouville 问题、以及一般的椭圆本征值问题。[12][15]

## 变分表征的推广与解释

**闭流形上的 Laplace–Beltrami 算子。** 在黎曼流形 $(M,g)$ 上，自然振动频率对应 Laplace–Beltrami 算子的谱；它是「振动鼓」物理图像的数学推广：流形的几何结构决定其谱的性质，而谱又反过来反映几何。[9]

**热方程与长时间行为。** 拉普拉斯算子的本征值与本征函数决定了热方程解的长时间行为——第一本征值控制衰减速率，本征函数给出空间模式。[6]

**非线性 PDE 中的应用。** 在非线性偏微分方程分析中，本征值变分表征用于稳态的稳定性判定，以及上解与下解的构造。[6]

**$L^\infty$ 型特征值问题。** 存在一个较少被讨论的变体：把 Rayleigh 商中的 $L^2$ 范数替换为 $L^\infty$ 范数，即 $\|\nabla u\|_{L^\infty}/\|u\|_{L^\infty}$，文献 [4] 刻画了与之相应的 $L^\infty$ 特征值问题。这提示「Rayleigh 商」的概念并非只有一种形式。

**数值与符号计算。** Wolfram Language 11 起内置了在一维区域上求解拉普拉斯算子本征值与本征函数的功能，例如求最小四个本征值与对应本征函数。[8]

## 与本站既有条目的关联

- 变分表征所依赖的能量泛函 $\int|\nabla u|^2$ 正是 [[扩散方程]]（$\rho_t = \rho_{xx}/2$）中空间算子的二次型；热方程的长时行为由第一本征值主导。[6]
- 由 Feynman–Kac 路径积分公式（[[费恩曼-卡茨公式]]）出发，热核的谱展开与本征值直接相关，可与 [[维纳过程]] 描述的扩散过程相对照。
- 该变分结构在量子力学中表现为「基态能量最小化」，与 [[量子过程的随机性]] 及 [[薛定谔]] 相关的表述相呼应。
- 就本征值问题的一般背景与历史脉络，可参考 [[数学指南-实用数学手册]] 中关于 [[随机过程]] 与算子谱的相关评注。

## 争议、歧义与空白

1. **极小极大原理与最小值原理的关系**：第一本征值既可写成「最小值」，也可写成 $k=1$ 的极小极大式；两条表述在文献中常被混用，需注意后者对 $k\ge 2$ 才是本质推广。[11][12]
2. **算子符号与边界条件约定不统一**：有的文献写 $\Delta u = \lambda u$（此时 $\lambda\le 0$），有的写 $-\Delta u = \lambda u$（$\lambda\ge 0$）。引用数值时必须核对约定。[8][10][11]
3. **区域正则性与谱的离散性**：极小极大公式的正当性依赖 $-\Delta$ 的自伴性与紧预解式；一般区域（如非光滑边界）上的 spectral 行为需要额外假设，检索到的资料大多略过了这一点。[3][11]
4. **$L^\infty$ 变体的理论地位**：[4] 提出的 $L^\infty$ 特征值问题与经典 $L^2$ Rayleigh 商在分析框架上差异明显，其与经典谱理论的联系尚不清楚。
5. **来源质量参差**：主要检索结果来自 StackExchange、MathOverflow、Wikipedia、知乎与机构讲座预告，缺乏教科书级权威推导。[1][6][7][13][14]

## 建议补充的文献

- Courant, R. & Hilbert, D.《数学物理方法》——极小极大原理的经典出处。
- Reed, M. & Simon, B., *Methods of Modern Mathematical Physics IV: Analysis of Operators*——紧自伴算子谱的严格处理。
- Chavel, I., *Eigenvalues in Riemannian Geometry*——Laplace–Beltrami 谱与几何的联系。[9]
- Davies, E. B., *Spectral Theory and Differential Operators*——一般区域上的谱理论与定义域问题。
- 就 L∞ 特征值问题，追查 [4] 所引 arXiv 原文及其后续引用。

## 参考文献

[1] Proof for the classical variational characterization of Dirichlet eigenvalues, math.stackexchange.com
[2] Rayleigh quotient, Wikipedia (en)
[3] Lectures 8+9: Laplacian Eigenvalue Problems for General Domains, math.ucdavis.edu
[4] Eigenvalue Problems in L∞, arXiv
[5] Rayleigh quotient and the maximum principle for eigenvalues, Chebfun
[6] 讲座预告｜数学探索第一期：拉普拉斯特征值秘境之旅，香港中文大学（深圳）
[7] 【线性代数系列】正定矩阵、Hermitian 矩阵与 Rayleigh quotient，知乎
[8] 拉普拉斯算子的本征值和本征函数：Wolfram 语言 11 的新功能，wolfram.com
[9] 拉普拉斯-贝尔特拉米算子的特征值与谱，Bohrium
[10] 拉普拉斯算子，维基百科（中文）
[11] Min-Max Characterisation of eigenvalues, ETH Zürich
[12] Min-max theorem, Wikipedia (en)
[13] Eigenvalues of the Laplacian and min-max formula in any space dimension, MathOverflow
[14] Min-Max Principle $\lambda_n = \inf_{X\in\Phi_n(V)}\{\sup_{u\in X}\cdots\}$, math.stackexchange.com
[15] The Min-Max and Max-Min Principle, loss.math.gatech.edu

## References

1. [Proof for the the classical variational characterization of Dirichlet ...](https://math.stackexchange.com/questions/4467190/proof-for-the-the-classical-variational-characterization-of-dirichlet-eigenvalue) — math.stackexchange.com
2. [Rayleigh quotient - Wikipedia](https://en.wikipedia.org/wiki/Rayleigh_quotient) — en.wikipedia.org
3. [[PDF] Lectures 8+9: Laplacian Eigenvalue Problems for General Domains](https://www.math.ucdavis.edu/~saito/courses/LapEig/lecpdf/lecture8+9.pdf) — math.ucdavis.edu
4. [[PDF] Eigenvalue Problems in L - arXiv](https://arxiv.org/pdf/2107.12117) — arxiv.org
5. [Rayleigh quotient and the maximum principle for eigenvalues - Chebfun](https://www.chebfun.org/examples/sphere/RayleighQuotientExample.html) — chebfun.org
6. [讲座预告｜数学探索第一期：拉普拉斯特征值秘境之旅](https://sse.cuhk.edu.cn/event/1547) — sse.cuhk.edu.cn
7. [【线性代数系列】正定矩阵Hermitian矩阵Rayleigh quotient 瑞利商矩阵 ...](https://zhuanlan.zhihu.com/p/675513135) — zhuanlan.zhihu.com
8. [拉普拉斯算子的本征值和本征函数: Wolfram语言11 的新功能](https://www.wolfram.com/language/11/differential-eigensystems/a-laplacians-eigenvalues-and-eigenfunctions.html.zh?footer=lang) — wolfram.com
9. [拉普拉斯-贝尔特拉米算子的特征值与谱| Bohrium](https://www.bohrium.com/sciencepedia/feynman/geometric_analysis_graduate-eigenvalues_and_spectra_of_the_Laplace-Beltrami_operator) — bohrium.com
10. [拉普拉斯算子- 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/%E6%8B%89%E6%99%AE%E6%8B%89%E6%96%AF%E7%AE%97%E5%AD%90) — zh.wikipedia.org
11. [[PDF] Min-Max Characterisation of eigenvalues - metaphor](https://metaphor.ethz.ch/x/2021/fs/401-3462-00L/sc/extras/Minmax.pdf) — metaphor.ethz.ch
12. [Min-max theorem - Wikipedia](https://en.wikipedia.org/wiki/Min-max_theorem) — en.wikipedia.org
13. [Eigenvalues of the Laplacian and min-max formula in any space ...](https://mathoverflow.net/questions/386196/eigenvalues-of-the-laplacian-and-min-max-formula-in-any-space-dimension) — mathoverflow.net
14. [Min-Max Principle $\lambda_n = \inf_{X \in \Phi_n(V)} \{ \sup_{u \in X ...](https://math.stackexchange.com/questions/1827876/min-max-principle-lambda-n-inf-x-in-phi-nv-sup-u-in-x-rhou) — math.stackexchange.com
15. [[PDF] THE MIN-MAX AND MAX-MIN PRINCIPLE Eigenvalues of linear ...](https://loss.math.gatech.edu/16FALLTEA/NOTES/minmax.pdf) — loss.math.gatech.edu

## Related
- [[queries/research-泊松方程与拉普拉斯方程椭圆型方程本体-2026-09-27-160108-research-186]]
