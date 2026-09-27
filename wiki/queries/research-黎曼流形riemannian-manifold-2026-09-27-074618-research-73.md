---
type: query
title: "Research: 黎曼流形（Riemannian manifold）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 黎曼流形（Riemannian manifold）

# 黎曼流形（Riemannian manifold）

## 概述

黎曼流形是带有**度量张量**（也称黎曼度量）的微分流形：它在每个点的切空间上光滑地指定一个内积，从而允许在流形上度量长度、角度与体积等几何量 [1][4][8]。其名称来源于 [[黎曼]]。与仅具有拓扑或微分结构的流形相比，黎曼流形多出一层"度量结构"，这使得距离、曲率、体积等概念可以在弯曲空间中严格定义 [5][8][10]。

## 形式定义

一个黎曼流形是一个二元组 $(M, g)$，其中 [2]：

- $M$ 是一个光滑流形；
- $g$ 是一个**黎曼度量**，即一个光滑的 2-张量场 $g \in \mathcal{T}^2(M)$，它是对称的（$g(X, Y) = g(Y, X)$）且正定的（若 $X \neq 0$ 则 $g(X, X) > 0$）[3]。

该度量在每个切空间 $T_pM$ 上确定一个内积，通常记作
$$\langle X, Y \rangle := g(X, Y), \qquad X, Y \in T_pM.$$
一个流形连同其给定的黎曼度量被称为黎曼流形；在不会引起混淆时，"metric" 常被直接用来指代黎曼度量 [3]。

## 度量张量的性质

由定义可直接导出以下性质：

- **对称性**：$g(X, Y) = g(Y, X)$ [3]。
- **正定性**：$g(X, X) > 0$ 对任意非零向量 $X$ 成立 [3]。
- **逐点内积**：$g$ 在每一点给出切空间上的内积，因而可计算向量场的长度、向量间的夹角与（配合体积形式时的）体积 [4][8]。
- **光滑依赖**：$g$ 作为张量场是光滑的，即内积随基点光滑变化 [2][3]。

在局部坐标系中，$g$ 由对称正定矩阵 $g_{ij} := \langle \partial_i, \partial_j \rangle$ 给出 [15]。

## 存在性

借助单位分解（partition of unity），可以证明**每一个光滑流形都可以被赋予一个黎曼度量** [3]。这意味着"可度量化"对流形并不构成额外的拓扑限制；黎曼几何的丰富性来自度量的选择而非其存在性。

## 典型例子

- **欧氏空间** $\mathbb{R}^n$ 配上标准内积，是最基本的黎曼流形 [1]。
- **子流形诱导度量**：若 $(\tilde{M}, \tilde{g})$ 是黎曼流形，$\iota: M \to \tilde{M}$ 是（浸入的）子流形，则诱导度量 $g = \iota^*\tilde{g}$ 是 $\tilde{g}$ 对切于 $M$ 的向量的限制。由于内积的限制仍是内积，$g$ 自动是 $M$ 上的黎曼度量 [3]。这一构造与[[微分形式拉回]]所用的拉回机制相同。典型情形是球面 $S^n \subset \mathbb{R}^{n+1}$ 上的标准度量 [3]。
- **乘积与商**：许多黎曼度量以子流形、乘积或商的方式自然产生 [3]。
- **李群**：李群上可构造左不变体积形式，从而得到黎曼几何结构，其相应测度为哈尔测度 [6]。

## 伪黎曼与半黎曼度量

**伪黎曼度量**（亦称**半黎曼度量**）是光滑流形上的对称 2-张量场 $g$，它在每点**非退化**：唯一与所有向量正交的向量是零向量，即 $g(X, Y) = 0$ 对所有 $Y \in T_pM$ 成立当且仅当 $X = 0$。在局部余标架下，非退化等价于矩阵 $g_{ij}$ 可逆 [3]。

- 若 $g$ 是黎曼的，则非退化性由正定性立即推出，因此**每个黎曼度量都是伪黎曼度量**；反之一般不成立，伪黎曼度量不必是正的 [3]。
- 伪黎曼度量的典型物理实例是洛伦兹度量（广义相对论），但收集到的来源未展开此方向。

## 由度量导出的几何结构

### 长度与距离

黎曼度量可以定义曲线的长度。给定黎曼流形 $M$、度量张量 $g$ 与连续可微曲线 $f: [a, b] \to M$，其长度为
$$L(f) = \int_a^b \sqrt{g_{f(t)}\left(\frac{\mathrm{d}f}{\mathrm{d}t}(t), \frac{\mathrm{d}f}{\mathrm{d}t}(t)\right)}\,\mathrm{d}t$$
[4]。距离则可由此下确界方式定义（源中未给出显式公式，见下文"空白"一节）。

### 测地线

测地线被描述为黎曼流形中两点之间的（弧长意义下）最短路径 [4]。它由测地线微分方程刻画：
$$\nabla_{\frac{\mathrm{d}\gamma}{\mathrm{d}t}} \frac{\mathrm{d}\gamma}{\mathrm{d}t} = 0,$$
用 Christoffel 符号写出即
$$\frac{\mathrm{d}^2 x^k}{\mathrm{d}t^2} + \Gamma^k{}_{ij} \frac{\mathrm{d}x^i}{\mathrm{d}t} \frac{\mathrm{d}x^j}{\mathrm{d}t} = 0$$
[4]。此处出现的联络是 **Levi-Civita 联络** [4]。

### 指数映射

给定点 $p$ 处的切向量 $v$，存在唯一的测地线 $G_v$ 与指数映射 $\exp$ 满足
$$G_v(0) = p, \qquad \nabla_v (G_v)(0) = v, \qquad \exp_p(v) = G_v(1)$$
[4]。指数映射把切空间的局部几何与流形的局部几何联系起来。

### 切向量与切空间

流形上一点处的切空间是该点所有切向量的集合，可类比为圆的切线或曲面的切平面；切向量可充当方向导数算子 [4]。

## 体积形式

### 黎曼体积形式

任何**可定向**的伪黎曼（含黎曼）流形都有一个自然的体积形式。在局部坐标下可写成
$$\omega = \sqrt{|g|}\,\mathrm{d}x^1 \wedge \dots \wedge \mathrm{d}x^n,$$
其中 $\mathrm{d}x^i$ 是构成流形余切丛的一组正向基的 1-形式，$|g|$ 是度量张量矩阵表示的行列式的绝对值 [6][13]。由于 $g_{ij}$ 在黎曼情形下正定，其行列式为正，因此也常直接写作
$$\mathrm{vol}_M = \sqrt{\det(g_{ij})}\,\mathrm{d}x^1 \wedge \dots \wedge \mathrm{d}x^n$$
[9][11][15]。在坐标 $x^1, \dots, x^n$ 下，若 $g_{ij} := \langle \partial_i, \partial_j \rangle$，则体积形式为 $\sqrt{\det(g)}\,\mathrm{d}x^1 \wedge \cdots \wedge \mathrm{d}x^n$，其中 $\det(g)$ 在每点 $p$ 等于矩阵 $(g_{ij}(p))$ 的行列式 [15]。

体积形式的等价记法包括
$$\omega = \mathrm{vol}_n = \varepsilon = \star(1),$$
其中 $\star$ 是 Hodge 星算子，$\star(1)$ 强调体积形式是流形上常数映射的霍奇对偶，它等于 Levi-Civita 张量 $\varepsilon$ [6][13]。

从线性代数角度看，内积空间 $V$ 上的体积形式是 $\Lambda^n V$ 中长度为 1 的一个元素；定向黎曼流形上的度量逐点确定这样的元素，因而整体地给出一个 $n$-形式 $\omega$ [15]。

### 定向与非定向情形

- 上述"自然体积形式"的表述要求流形可定向 [13]。
- 体积形式的绝对值是一个**体积元**（volume element），也称为**扭曲体积形式**或**伪体积形式**；它同样定义测度，并且在**任何**微分流形上存在，无论是否可定向 [13]。

### 与之相关的特例

- **辛流形**：任何辛流形（更确切地说，殆辛流形）有自然的体积形式。若 $M$ 是带辛形式 $\omega$ 的 $2n$ 维流形，由非退化性知 $\omega^n$ 处处非零，故任何辛流形可定向（事实上已定向）[6]。
- **李群**：可定义由左平移拉回的体积形式 $\omega_g = L_g^*\omega_e$，它在相差一个常数的意义下唯一，相应测度为哈尔测度；作为推论，任何李群都是可定向的 [6]。
- **Kähler 流形**：Kähler 流形作为复流形天然可定向，因而具有体积形式；若一个流形既是辛的又是黎曼的，则在 Kähler 情形下两种方式定义的体积形式相等 [6][13]。
- **曲面的体积形式**：对嵌入 $n$ 维欧氏空间的 2 维曲面 $\phi: U \subset \mathbb{R}^2 \to \mathbb{R}^n$，欧氏度量诱导出 $U$ 上的度量，其度量矩阵分量为 $\lambda_{ij} = \partial \phi_i / \partial u_j$ 的相应组合，进而给出曲面的面积元 [6]。

### 整体不变量

连通流形上一个体积形式有一个唯一的整体不变量，即**总体积** $\mu(M)$，它在保持体积形式的映射下不变。总体积可以是无穷，例如 $\mathbb{R}^n$ 上的勒贝格测度。对不连通流形，各连通分支的体积是不变量 [6]。体积形式还提供了在微分流形上对函数积分的手段，即定义一个可用勒贝格积分处理的测度 [13]。

## 符号说明与常见混淆

- 希腊字母 $\omega$ 常被用来表示体积形式，但该记法并不通用：符号 $\omega$ 在微分几何中有其他含义（例如辛形式），因此公式中的 $\omega$ 不一定指体积形式 [6]。

## 空白、矛盾与待澄清之处

1. **记号 $|g|$ 的歧义**：英文源 [13] 明确把 $|g|$ 定义为度量张量行列式的绝对值，而中文与教材式来源 [9][11][15] 直接写 $\sqrt{\det(g_{ij})}$ 而不取绝对值。对黎曼（正定）度量而言二者无实质差别，但对伪黎曼度量必须取绝对值 [13]，这一点在部分来源中未加区分。
2. **可定向性要求**：体积形式的"自然存在性"要求可定向 [13]，而另一些来源 [6] 直接给出公式而未强调该前提。非可定向情形需要退回到伪体积形式/扭曲体积形式 [13]，这一区分在本组来源中仅由 [13] 给出。
3. **曲率内容缺失**：来源 [3] 的书名是 *Riemannian Manifolds: An Introduction to Curvature*，但收集到的摘录只覆盖度量定义、伪黎曼度量与子流形诱导度量，未包含黎曼曲率张量、截面曲率、Ricci 曲率、标量曲率等核心内容。因此本页暂无法给出曲率部分的系统叙述。
4. **测地线的"最短"表述**：来源 [4] 称测地线是"两点间最短路径"，但严格的测地线只保证局部最短，整体最短性需要完备性条件（如 Hopf–Rinow 定理），本组来源未给出该限定。
5. **距离函数的定义**：来源 [4] 给出长度泛函 $L(f)$，但未给出两点距离 $d(p, q)$ 作为长度下确界的显式定义 [8] 仅笼统提到"可以定义距离"。
6. **黎曼流形与复几何的桥接**：本组来源未涉及黎曼流形与[[黎曼面]]（一维复流形）在共形结构意义上的联系，也未涉及[[共形映射]]在一般黎曼流形上的推广，这构成与本 wiki 既有条目之间的一处未连接点。
7. **历史来源**：来源 [3] 提到"任意流形都可赋予黎曼度量"的练习，但未给出 [[黎曼]] 1854 年就职演讲等历史出处。

## 建议补充的来源

- do Carmo, *Riemannian Geometry* —— 系统覆盖曲率、测地线完备性与比较定理。
- John M. Lee, *Introduction to Riemannian Manifolds* —— 第 4 章起关于曲率的完整处理，可与 [3] 配合。
- Hopf–Rinow 定理的专门条目，用于补足"测地线最短性"与"指数映射满射性"的严谨条件。
- Nash 嵌入定理相关文献，用于说明任意黎曼流形可否等距嵌入欧氏空间。
- 关于 [[高斯]] 绝妙定理（Gauss's Theorema Egregium）与内蕴曲率的材料。
- 关于洛伦兹流形与广义相对论的材料，用于补足伪黎曼度量一节目前仅有定义而无实例的空白。

## 相关条目

- [[黎曼]] —— 黎曼流形的命名来源与奠基者
- [[黎曼面]] —— 一维复流形，与二维黎曼几何关系密切
- [[微分形式拉回]] —— 诱导度量 $g = \iota^*\tilde{g}$ 所用的拉回机制
- [[共形映射]] —— 黎曼度量之间的共形等价类
- [[高斯]]、[[外尔]]、[[克莱因]]、[[庞加莱]] —— 与本主题相关的数学史人物

## References

1. [Metric tensor](https://en.wikipedia.org/wiki/Metric_tensor) — en.wikipedia.org
2. [RIEMANN METRIC TENSOR ❤️🌹♥️ Bernhard ...](https://www.facebook.com/100094746404967/posts/riemann-metric-tensor-%EF%B8%8F%EF%B8%8Fbernhard-riemanns-1854-habilitation-lecture-introduced-t/901832849651587) — facebook.com
3. [Riemannian Manifolds: An Introduction to Curvature](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/leeriemm.pdf) — webhomes.maths.ed.ac.uk
4. [Riemannian Manifolds: Foundational Concepts](https://patricknicolas.substack.com/p/riemannian-manifolds-1-foundation) — patricknicolas.substack.com
5. [Metrics and Riemannian Manifolds | Springer Nature Link](https://link.springer.com/chapter/10.1007/978-3-031-97973-6_3) — link.springer.com
6. [体积形式 - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/%E4%BD%93%E7%A7%AF%E5%BD%A2%E5%BC%8F) — zh.wikipedia.org
8. [黎曼几何与黎曼流形](https://blog.csdn.net/m0_55196097/article/details/130510516) — blog.csdn.net
9. [黎曼流形(Riemannian manifolds)体积元形式](https://zhuanlan.zhihu.com/p/496204505) — zhuanlan.zhihu.com
10. [黎曼几何与度量张量原创](https://blog.csdn.net/qq_41375318/article/details/145536716) — blog.csdn.net
11. [Surface measure : r/math](https://www.reddit.com/r/math/comments/2a3up2/surface_measure) — reddit.com
13. [Volume form - Wikipedia](https://en.wikipedia.org/wiki/Volume_form) — en.wikipedia.org
15. [riemannian geometry, spring 2013, homework 8](https://math.uchicago.edu/~dannyc/courses/riem_geo_2013/homework8.pdf) — math.uchicago.edu

## Related
- [[queries/research-黎曼几何中的体积测度理论标准文献与-212-核实-2026-09-27-074618-research-74]]
