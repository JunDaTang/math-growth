---
type: query
title: "Research: 李超代数（Lie superalgebra）尚无条目"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 李超代数（Lie superalgebra）尚无条目

# 李超代数（Lie superalgebra）

**李超代数**（英语：Lie superalgebra）是[[李代数]]在 $\mathbb{Z}_2$-分次框架下的自然推广。与普通李代数不同，李超代数的载体空间带有**偶**（even/bosonic）与**奇**（odd/fermionic）两类元素的区分，其李括号（**超括号**或**超交换子**）同时含交换子与反交换子结构，遵守**分次反对称性**与**分次雅可比恒等式**[1][2][5][6]。

李超代数在理论物理中作为**超对称**（supersymmetry）的数学基础：偶元素对应玻色子，奇元素对应费米子[1][6]。历史上由 F. A. Berezin、V. G. Kac、Yu. I. Manin、D. A. Leites 等人奠基，Kac 在 1977 年完成了有限维单李超代数的分类[1][5]。李超代数现已成为李理论、超几何学（supergeometry）与弦理论的重要交叉领域。

## 前置概念

### Grassmann 代数与超代数

**Grassmann 代数** $\Lambda(\xi^1, \ldots, \xi^q)$ 是由奇生成元 $\xi^\alpha$ 生成的代数，满足
$$\xi^\alpha \xi^\beta = -\xi^\beta \xi^\alpha \quad \Longrightarrow \quad (\xi^\alpha)^2 = 0$$

定义中的 $\mathbb{Z}_2$-分次结构为 $\Lambda = \Lambda_0 \oplus \Lambda_1$，其中偶部分由偶数个生成元的乘积张成，奇部分由奇数个生成元的乘积张成[7][16]。

一个 **$\mathbb{Z}_2$-分次超代数**（或简称**超代数**）是带直和分解 $A = A_0 \oplus A_1$ 的结合含幺代数，满足 $A_i A_j \subseteq A_{i+j}$（下标按模 2 理解）。齐次元素 $x$ 的**奇偶性**记作 $|x| \in \{0, 1\}$。结合超代数 $A$ 称为**超交换的**（supercommutative），若
$$yx = (-1)^{|x||y|} xy$$

对任意齐次元素 $x, y \in A$ 成立。该符号规则称为 **Koszul 符号规则**，构成整个超数学的基石[7][16]。

### $\mathbb{Z}$-分次李代数

先引入更宽泛的概念：**$\mathbb{Z}$-分次李代数**是 $\mathbb{Z}$-分次向量空间 $g = \bigoplus_{\alpha \in \mathbb{Z}} g(\alpha)$，连同双线性映射 $[\cdot, \cdot]: g \times g \to g$ 满足
- $[g(\alpha), g(\beta)] \subseteq g(\alpha+\beta)$
- $[a, b] = -(-1)^{\alpha\beta}[b, a]$
- $(-1)^{\alpha\gamma}[a, [b, c]] + (-1)^{\alpha\beta}[b, [c, a]] + (-1)^{\beta\gamma}[c, [a, b]] = 0$，

其中 $a \in g(\alpha), b \in g(\beta), c \in g(\gamma)$。任何 $\mathbb{Z}$-分次李代数均可由"折叠"（rolling-up）方式赋予 $\mathbb{Z}_2$-分次结构：$g_0 = \bigoplus g(2\alpha), g_1 = \bigoplus g(2\alpha+1)$。但此种"折叠"得到的 $\mathbb{Z}_2$-分次通常不称为"超"[1][2]。

此外，$\mathbb{Z}_2$-分次与**上同调来源的 $\mathbb{Z}_2$-分次**是两回事：前者称为**超分次**（super gradation），后者称为**上同调分次**（cohomological gradation），两者须相容。Pierre Deligne 对此区分有专门讨论[1][12]。

## 形式定义

设 $K$ 为特征不为 2、3 的域（通常取 $\mathbb{R}$ 或 $\mathbb{C}$）。定义中的共同约定是：若 $v$ 出现在任何公式中，则自动假设 $v$ 是齐次元素（称**度约定**，degree convention）[2]。

**李超代数** $g = g_0 \oplus g_1$ 是 $\mathbb{Z}_2$-分次向量空间，配备双线性映射 $[\cdot, \cdot]: g \times g \to g$（称为**李超括号**或**超交换子**），满足：

1. **$\mathbb{Z}_2$-分次兼容性**：$[g_\alpha, g_\beta] \subseteq g_{\alpha+\beta}$，$\alpha, \beta \in \mathbb{Z}_2$。
2. **分次反对称性**（graded skew-symmetry）：
$$[x, y] = -(-1)^{|x||y|}[y, x] \quad \text{或写成} \quad [x, y] = -(-1)^{|x||y|}[y, x]$$
3. **分次雅可比恒等式**（graded Jacobi identity）：
$$(-1)^{|x||z|}[x, [y, z]] + (-1)^{|y||x|}[y, [z, x]] + (-1)^{|z||y|}[z, [x, y]] = 0$$

这里 $x, y, z$ 均为齐次元素，$|x|$ 表示 $x$ 的度（0 或 1），$[x, y]$ 的度是 $|x| + |y| \pmod 2$[1][2][3][5][6]。

**附加公理**（可选的等价形式）：当 $2$ 可逆时 $|x| = 0$ 情形下 $[x, x] = 0$ 自动成立；当 $3$ 可逆时 $|x| = 1$ 情形下 $[[x, x], x] = 0$ 自动成立。当基环为整数环或李超代数为自由模时，这些条件等价于 [[queries/庞加莱-伯克霍夫-威特定理]]（PBW 定理）成立的必要条件[1][2]。

### 等价表述

用双线性性展开 $[x+y, x+y]$，从反对称性可得反交换律
$$[x, y] + [y, x] = 0$$
但这仅在偶元素之间成立；对两个奇元素的括号则**对称**，即 $[x, y] = [y, x]$，等价于反交换子 $\{x, y\} = xy + yx$[1][7][15]。

## 基本性质

### 偶部与奇部

设 $g = g_0 \oplus g_1$ 为李超代数。通过分析分次雅可比恒等式并根据参与括号的奇元素个数分类，可得到四种情形[1][6]：

1. **无奇元素**：$g_0$ 为普通[[李代数]]。
2. **一个奇元素**：$g_1$ 是 $g_0$ 的线性表示，作用由 $\mathrm{ad}_a: b \mapsto [a, b]$（$a \in g_0, b \in g_1$）给出。
3. **两个奇元素**：括号 $[\cdot, \cdot]: g_1 \otimes g_1 \to g_0$ 是**对称**的 $g_0$-等变映射。
4. **三个奇元素**：对所有 $b \in g_1$ 都有 $[b, [b, b]] = 0$。

因此：
- $g_0$ 自身构成一个普通[[李代数]]；
- $g_1$ 是 $g_0$ 的线性表示；
- 存在对称的 $g_0$-等变线性映射 $\{\cdot, \cdot\}: g_1 \otimes g_1 \to g_0$，满足
$$[\{x, y\}, z] + [\{y, z\}, x] + [\{z, x\}, y] = 0, \quad x, y, z \in g_1$$

具体地说：
- **偶-偶、偶-奇**括号在奇偶性稳定条件下就是普通李括号的推广；
- **奇-奇**括号变为**反交换子**，是超对称理论中"两个费米子给出一个玻色子"的代数体现。

条件 (1)–(3) 是**线性**的，可归约为普通李代数问题；条件 (4) 是**非线性**的，是从普通李代数与表示出发构造李超代数时最难验证的部分[1]。

### 超导子

设 $A$ 是（不必结合的）$\mathbb{Z}_2$-分次代数。次数为 $\alpha$ 的线性映射 $\partial: A \to A$ 称为**左超导子**（left superderivation），若
$$\partial(bc) = \partial(b) c + (-1)^{\alpha b} b \partial(c), \quad b, c \in A$$

类似可定义**右超导子**。次 0（次 1）的超导子称为**偶超导子**（偶导子，even derivation）或**奇超导子**。所有超导子构成的集合 $\mathrm{Sder}(A)$ 是 $\mathrm{End}_K A$ 的李子超代数[2]。

### 引理（分次雅可比性的等价表述）

设 $A$ 是 $\mathbb{Z}_2$-分次代数，乘积 $(a, b) \mapsto [a, b]$ 分次反对称。则以下等价：
(a) $A$ 满足分次雅可比恒等式；
(b) 对所有 $a \in A$，映射 $\mathrm{ad}_a: b \mapsto [a, b]$ 是度数为 $|a|$ 的左超导子；
(c) 对所有 $a \in A_\alpha$，映射 $\mathrm{ad}_a: b \mapsto [b, a]$ 是度数为 $|a|$ 的右超导子[2]。

### 理想与单性

设 $g$ 为李超代数，$V, W \subseteq g$ 为子空间，$[V, W]$ 表示由所有 $[v, w]$（$v \in V, w \in W$）张成的子空间。

- $\mathbb{Z}_2$-分次子空间 $a \subseteq g$ 称为**左理想**（left ideal），若 $[g, a] \subseteq a$；
- 称为**理想**，若 $[a, g] \subseteq a$（注意 $a$ 为 $\mathbb{Z}_2$-分次）。

李超代数称为**单的**（simple），若它非交换且除 $0$ 与 $g$ 外没有其他 $\mathbb{Z}_2$-分次理想[2][5]。

**命题**：单李超代数中唯一的左理想是 $0$ 和 $g$[2]。

**命题**：设 $g$ 为单李超代数。则
(a) 任何不变双线性形式要么非退化，要么为零；
(b) 任何不变双线性形式是**超对称的**，即 $(a, b) = (-1)^{|a||b|}(b, a)$；
(c) 任何两个非零不变双线性形式成比例；
(d) 不变双线性形式要么全为偶，要么全为奇[2]。

## 对合与 ∗-李超代数

**∗-李超代数**是指复李超代数 $g$ 配备反线性对合 $*: g \to g$，它保持 $\mathbb{Z}_2$-分次，且满足
$$[x, y]^* = [y^*, x^*]$$
或采用另一约定 $[x, y]^* = (-1)^{|x||y|}[y^*, x^*]$（两者通过将 $*$ 改为 $-*$ 互换）。其泛包络代数将是通常的 ∗-代数[1][6][10]。

## 例子

### 结合超代数上的超交换子

给定结合超代数 $A$，可在齐次元素上定义
$$[x, y] = xy - (-1)^{|x||y|} yx$$
再线性延拓至整个 $A$，则 $A$ 与超交换子一起构成李超代数[2][5][7]。

**最简单例子**：$A = \mathbf{End}(V)$ 是超向量空间 $V = \mathbb{K}^{p|q}$ 的自同态代数，其李超代数记作 $\mathfrak{gl}(p|q)$ 或 $\mathfrak{gl}(m|n)$。有
$$\mathfrak{gl}(m|n)_0 \cong \mathfrak{gl}(m) \oplus \mathfrak{gl}(n)$$
$$\mathfrak{gl}(m|n)_1 \cong (\mathbb{C}^m \otimes \mathbb{C}^{n*}) \oplus (\mathbb{C}^{m*} \otimes \mathbb{C}^n)$$

作为 $g_0$-模[3]。

### 一般线性李超代数

分块矩阵 $M = \begin{pmatrix} A & B \\ C & D \end{pmatrix}$（$A$ 为 $m\times m$，$D$ 为 $n\times n$），其中 $A, D$ 偶、$B, C$ 奇，构成 $\mathfrak{gl}(m|n)$。定义**超迹**为
$$\mathrm{str}(M) = \mathrm{tr}(A) - \mathrm{tr}(D)$$

超迹满足 $\mathrm{str}([M, N]) = 0$ 对所有 $M, N \in \mathfrak{gl}(m|n)$ 成立[3][5]。

### 特殊线性李超代数

$\mathfrak{sl}(m|n) = \{M \in \mathfrak{gl}(m|n) : \mathrm{str}(M) = 0\}$ 是 $\mathfrak{gl}(m|n)$ 的余一维李子超代数[3][5]。当 $m \neq n$ 时它是单的；当 $m = n$ 时，单位矩阵 $I_{2m}$ 生成一个理想，其商 $\mathfrak{psl}(m|m) = \mathfrak{sl}(m|m)/\langle I_{2m}\rangle$ 当 $m \geq 2$ 时是单的[1][2][5]。

### 正交辛李超代数

考虑 $\mathbb{C}^{m|2n}$ 上的非退化、偶、超对称双线性形式 $\langle \cdot, \cdot \rangle$，定义
$$\mathfrak{osp}(m|2n) = \{X \in \mathfrak{gl}(m|2n) \mid \langle Xu, v\rangle + (-1)^{|X||u|}\langle u, Xv\rangle = 0, \forall u, v\}$$

其偶部分为 $\mathfrak{so}(m) \oplus \mathfrak{sp}(2n)$[1][6]。当 $m \geq 1, n \geq 1$ 时（参数约定随文献而略有差异）$\mathfrak{osp}(m|2n)$ 是单的[4][5]。

### 第二类结构：gl̆(m), sl̆(m) 与 P(n), Q(n)

考虑分块矩阵 $\begin{pmatrix} A & B \\ B & A \end{pmatrix}$（$m = n$，$A_1 = A_0, B_1 = B_0$）与迹条件可构造 $\mathfrak{gl}^{e}(m)$ 与 $\mathfrak{sl}^{e}(m)$；对偶进一步定义**奇怪系列** $P(n)$ 与 $Q(n)$（也称"奇异序列"或 Michal–Radicati 的 $f$-$d$ 代数）[1][4][5][6]。

$P(n)$ 的奇部在奇偶变换下无类似物，构成所谓"奇怪的超代数"[8]。

### Poisson 超代数与 Whitehead 积

- **Poisson 超代数**：结合代数同时带有李括号与"普通"乘积的代数结构。
- **Whitehead 积**：同伦群上的 Whitehead 积给出整数上的李超代数例子。
- **超庞加莱代数**：生成平面超空间的等距[1][6]。

## 分类

### 有限维单复李超代数（Kac 分类）

V. G. Kac（与 Nahm–Rittenberg–Scheunert 独立地，[SNR76a], [SNR76b]）分类了有限维单复李超代数。除普通李代数（$g_1 = 0$ 情形）外，**经典型**（classical type）单李超代数包括以下系列[1][2][5]：

**A 系列**：
- $A(m, n) = \mathfrak{sl}(m+1, n+1)$，$m > n \geq 0$
- $A(n, n) = \mathfrak{psl}(n+1, n+1)$，$n \geq 1$

**B、C、D 系列**：
- $B(m, n) = \mathfrak{osp}(2m+1, 2n)$，$m \geq 0, n > 0$
- $C(n) = \mathfrak{osp}(2, 2n-2)$，$n \geq 2$
- $D(m, n) = \mathfrak{osp}(2m, 2n)$，$m \geq 2, n \geq 1$

**例外李超代数**：
- $D(2, 1; \alpha)$：$(9|8)$ 维（总维数 $17$）的连续族，$D(2, 1) = \mathfrak{osp}(4|2)$ 的变形。当 $\alpha \neq 0, -1$ 时是单的；在 $\alpha \mapsto \alpha^{-1}$ 与 $\alpha \mapsto -1-\alpha$ 生成的群轨道下同构[1][5][6]。
- $F(4)$：维数 $(24|16)$（总维数 $40$），偶部为 $\mathfrak{sl}(2) \oplus \mathfrak{so}(7)$[1][5][6]。
- $G(3)$：维数 $(17|14)$（总维数 $31$），偶部为 $\mathfrak{sl}(2) \oplus G_2$[1][5][6]。

**奇怪系列**：$P(n)$ 与 $Q(n)$，$n \geq 2$[1][5]。

**Cartan 型**：分为四族 $W(n), S(n), \widetilde{S}(2n), H(n)$。对于 Cartan 型单李超代数，奇部在偶部作用下不再**完全可约**[1][6]。Cartan 型李超代数可由反交换变量的向量场（而非通常情况的"联络型"李代数）实现，且当无交换型生成元时是有限维的[5]。

以上这些李超代数正是可以构造为**反变李超代数**（contragredient Lie superalgebra）$G(A, \tau)/C$ 的那些[2][5]。

### 经典单李超代数的子类

- **basic 型**：具有偶、非退化、$g$-不变双线性形式的经典单李超代数。这类正是可以构造为反变李超代数的那些，且其 Cartan 子代数 $h = h_0$[2]。
- **Type I**：$g_1 = g_1^+ \oplus g_1^-$ 为两个单 $g_0$-子模直和。包括 $A(m, n), C(n), P(n)$ 系列，满足 $[g_1^\pm, g_1^\pm] = 0$[2]。

### 无穷维简单线性紧李超代数

分类包含 10 个系列 $W(m, n)$、$S(m, n)$（$(m, n) \neq (1, 1)$）、$H(2m, n)$、$K(2m+1, n)$、$HO(m, m)$（$m \geq 2$）、$SHO(m, m)$（$m \geq 3$）、$KO(m, m+1)$、$SKO(m, m+1; \beta)$（$m \geq 2$）、$\widetilde{SHO}(2m, 2m)$、$\widetilde{SKO}(2m+1, 2m+3)$ 及 5 个例外代数[1][6]：

$$E(1, 6), E(5, 10), E(4, 4), E(3, 6), E(3, 8)$$

据 Kac 所述，最后两个特别有趣，因为它们的零级代数是标准模型规范群 $SU(3) \times SU(2) \times U(1)$。无穷维（仿射）李超代数在超弦理论中作为重要对称性出现；带超对称的 Virasoro 代数为 $K(1, \mathcal{N})$，只有当 $\mathcal{N} = 4$ 时才具中心扩展[1][6]。

### 关于 Killing 型

与简单李代数不同，有限维单李超代数的 **Killing 型**可能退化。Kac 的分类通过区分 **Killing 型非退化** 与 **Killing 型为零** 两种情形来分情形处理。Killing 型为零的情形包括 $A(n, n), D(n+1, n), D(2, 1; \alpha), P(n), Q(n)$[5]。

## 结构与表示理论

### 根系与根空间分解

设 $g$ 为 basic 经典单李超代数，$h = h_0$ 为 Cartan 子代数。定义根集 $\Delta = \Delta_0 \cup \Delta_1$（$\Delta_0$ 为偶根，$\Delta_1$ 为奇根）。进一步区分：

$$\Delta_0' = \{\alpha \in \Delta_0 : \alpha/2 \in \Delta_1\}, \quad \Delta_1' = \{\alpha \in \Delta_1 : 2\alpha \in \Delta_0\}$$

奇根 $\alpha$ 若满足 $(\alpha, \alpha) = 0$ 则称为**迷向**（isotropic）。$\alpha$ 迷向当且仅当 $\alpha \in \Delta_1'$（即 $2\alpha \notin \Delta_0$）[2][3]。

在例 $\mathfrak{gl}(m|n)$ 中，所有奇根都是迷向的；偶根则对应 $g_0 = \mathfrak{gl}(m) \oplus \mathfrak{gl}(n)$ 的根，具有正定的 Killing 型[3]。

### 三角分解与 Verma 模

给定三角分解 $g = n^- \oplus h \oplus n^+$（$b = h \oplus n^+$ 为 Borel 子代数），定义 **Verma 模**
$$M^\#(\lambda) = U(g) \otimes_{U(b)} V_\lambda$$

其中 $V_\lambda$ 是有限维分次单 $b$-模，满足 $n^+ V_\lambda = 0$ 且 $hv = \lambda(h)v$。Verma 模有唯一的极大分次子模，其商 $L(\lambda)$ 为单的。非零的因子模称为由最高权向量生成的模[2]。

对于 $q(n)$，任何有限维分次单 $b$-模 $V_\lambda$ 是一维的[2]。

对 $\mathfrak{gl}(m|n)$ 引入 **Kac 模**
$$K_\lambda = U(g) \otimes_{U(p)} L_\lambda(g_0) \cong \wedge^\bullet g_{-1} \otimes L_\lambda(g_0)$$

（$p = g_0 \oplus g_1^+$），它是有限维的（对整权），且有唯一（至多相差系数）满射 $K_\lambda \twoheadrightarrow L_\lambda$[3]。

### Category $\mathcal{O}$ 与中心特征

**Category $\mathcal{O}$** 由满足以下条件的 $U(g)$-模组成：
- （权模）$M = \bigoplus_{\mu \in h^*_0} M_\mu$；
- 对所有 $v \in M$，$\dim U(n_0^+)v < \infty$；
- $M$ 为有限生成的 $U(g)$-模。

Category $\mathcal{O}$ 具有足够投射对象（enough projectives），每个 block 只有有限个不可分解投射对象。每个 block 自然带分次结构，其分次平移函子与分次投射对象的组合可由 Hecke 代数与 Kazhdan–Lusztig 理论描述[2]。

### 中心与 Harish-Chandra 投影

**中心** $Z(g) = Z(g)_0 \oplus Z(g)_1$ 实际几乎总是 $Z(g)_0$（即 $Z(g)$ 无奇元素）。**（超）对称化映射** $S(g) \to U(g)$ 是 $g$-模同构，诱导线性同构 $S(g)^g \xrightarrow{\sim} Z(g)$[3]。

**Harish-Chandra 投影** $\zeta: U(g) \to U(h) = S(h)$ 通过分解 $U(g) = U(h) \oplus (n^-U(g) + U(g)n^+)$ 定义。对 $z \in Z(g)$ 与 $\lambda \in h^*$，中心特征 $\chi_\lambda(z) = \zeta(z)(\lambda)$[2]。

### Casimir 元素

设 $x_1, \ldots, x_n$ 与 $y_1, \ldots, y_n$ 是双基（满足 $(x_i, y_j) = \delta_{ij}$，且 $x_i, y_i$ 为同度数齐次元素），定义
$$\Omega = \sum_i (-1)^{\beta_i} x_i y_i \in U(g)$$

则 $\Omega$ 在 $U(g)$ 中是中心元素，称为 **Casimir 元素**。在 Verma 模 $M^\#(\lambda)$ 上 $\Omega$ 的作用为标量 $(\lambda + 2\rho, \lambda)$[2]。

### 典型（typical）与不典型（atypical）

最高权 $\lambda$ 称为**典型**（typical），若 $(\lambda + \rho, \alpha) \neq 0$ 对一切迷向奇根 $\alpha$ 成立，其中 $\rho = \rho_0 - \rho_1$（$\rho_0$ 为偶正根半和，$\rho_1$ 为奇正根半和）[3][14][15]。

**Kac 特征公式**：对典型权 $\lambda - \rho$（$L_\lambda$ 有限维），有
$$\chi_{L_\lambda} = \frac{\prod_{\alpha \in \Phi_1^+} (e^{\alpha/2} - e^{-\alpha/2})}{\prod_{\alpha \in \Phi_0^+} (e^{\alpha/2} - e^{-\alpha/2})} \sum_{w \in W} (-1)^w e^{w(\lambda+\rho)}$$

对典型 $\lambda$，Kac 模 $K_\lambda = L_\lambda$ 是单的。**非典型**（atypical）表示则表现出更丰富、更复杂的行为[3][15]。

### 奇数反射与 Serganova 理论

除 Weyl 群反射 $s_\alpha$ 外，还有**奇数反射**（odd reflections）$r_\alpha$：对迷向奇根 $\alpha$，
$$\Phi^+_\alpha := \{-\alpha\} \cup \Phi^+ \setminus \{\alpha\}$$
即用 $-\alpha$ 替换 $\alpha$。相应单根系 $Σ_\alpha = \{-\alpha\} \cup \{\beta \in Σ : (\beta, \alpha) = 0, \beta \neq \alpha\} \cup \{\beta + \alpha : \beta \in Σ, (\beta, \alpha) \neq 0\}$。

Serganova 定理：奇数反射 $r_\alpha$ 与 Weyl 群作用合起来在基本系集上传递[3]。

## 范畴论定义

在[[queries/范畴论]]中，李超代数可定义为非结合超代数，其积 $[\cdot, \cdot]$ 满足：

1. $[\cdot, \cdot] \circ (\mathrm{id} + \tau_{A,A}) = 0$
2. $[\cdot, \cdot] \circ ([\cdot, \cdot] \otimes \mathrm{id}) \circ (\mathrm{id} + \sigma + \sigma^2) = 0$

其中 $\sigma$ 是循环置换辫
$$\sigma = (\mathrm{id} \otimes \tau_{A,A}) \circ (\tau_{A,A} \otimes \mathrm{id})$$

这里 $\tau_{A,A}: A \otimes A \to A \otimes A$ 是交换同构，作用为 $\tau(a \otimes b) = (-1)^{|a||b|} b \otimes a$[1][6]。

这一范畴表述将李超代数纳入 Deligne 与 Morgan 发展的**超线性代数**框架。在此框架中，Koszul 符号规则被"隐藏"在张量范畴的交换同构中，因此许多经典代数结果可移植到超情形[12]。

### 泛包络代数与 Hopf 结构

李超代数的**泛包络代数** $U(g)$ 可赋予 Hopf 超代数结构。上积 $\Delta: U(g) \to U(g) \otimes U(g)$ 由对角映射 $\Delta(a) = a \otimes 1 + (-1)^{|a|} 1 \otimes a$ 定义。$U(g)$ 满足 PBW 定理：若 $a_1, \ldots, a_m$ 是 $g_0$ 的基，$b_1, \ldots, b_n$ 是 $g_1$ 的基，则
$$a_1^{i_1} \cdots a_m^{i_m} b_1^{j_1} \cdots b_n^{j_n}, \quad j_k \in \{0, 1\}$$
构成 $U(g)$ 的基[2][5][14]。

## 与物理的联系

### 超对称

李超代数最重要的物理联系是**超对称**（supersymmetry）。在超对称理论中：
- 偶元素 ↔ 玻色子（bosons，整数自旋）
- 奇元素 ↔ 费米子（fermions，半整数自旋）

超对称代数中既有交换子（玻色型生成元之间）又有反交换子（费米型生成元之间），因此属于李超代数范畴。典型的 N=1 超对称代数：
$$\{Q_\alpha, \bar{Q}_{\dot\beta}\} = 2\sigma^\mu_{\alpha\dot\beta} P_\mu, \quad [Q_\alpha, P_\mu] = 0, \quad \{Q_\alpha, Q_\beta\} = 0$$

在扩展超对称（$N > 1$）中还有**中心荷**：
$$\{Q_\alpha^I, Q_\beta^J\} = \epsilon_{\alpha\beta} Z^{IJ}, \quad Z^{IJ} = -Z^{JI}$$

$N=1$ 时无中心荷[11][14][15][17]。

**Haag–Lopuszanski–Sohnius 定理**（超庞加莱代数的一般性）：超级代数（superalgebra）是唯一可能的、将 Poincaré 代数通过费米型生成元非平凡扩展的代数结构——即唯一避开 Coleman–Mandula 定理而保持非平凡散射的对称性[11][15][17]。

### 超场与超空间

**超空间**（superspace）是把 Minkowski 空间用 Grassmann 旋量坐标 $\theta^\alpha, \bar{\theta}^{\dot\alpha}$ 扩展。其上函数（**超场**）自然包含玻色型与费米型分量：

- **手征超场**（chiral superfield）：满足 $\bar{D}_{\dot\alpha} \Phi = 0$，可展开为 $\Phi = \phi(y) + \sqrt{2} \theta \psi(y) + \theta\theta F(y)$（$y^\mu = x^\mu + i\theta\sigma^\mu\bar\theta$）；
- **反手征超场**：满足 $D_\alpha \Psi = 0$；
- **实（矢量）超场**：$V = V^\dagger$。

超对称不变作用量可通过 $\int d^4\theta$（D-项）和 $\int d^2\theta$（F-项）构造[11][15][17]：

$$\mathcal{L} = \int d^2\theta\, d^2\bar\theta\, K(\Phi, \Phi^\dagger) + \left[\int d^2\theta\, W(\Phi) + \mathrm{h.c.}\right] + \left[\int d^2\theta\, f_{ab} W^{\alpha a} W_\alpha^b + \mathrm{h.c.}\right]$$

其中 $K$ 为 **Kähler 势**，$W$ 为 **超势**（superpotential，必然是手征超场 $\Phi$ 的全纯函数）[17]。

### Wess–Zumino 模型与超 Yang–Mills

**Wess–Zumino 模型**是最简单的四维超对称场论，由复标量 $\phi$、Weyl 费米子 $\psi$ 与辅助场 $F$ 构成。其超势典型形式为 $W = \frac{1}{2}m\Phi^2 + \frac{1}{3}\lambda\Phi^3$。

**超 Yang–Mills 理论**将 Yang–Mills 规范场与伴随表示费米子（**gaugino**，即 gluino、photino 等）耦合。超场强度为
$$W_\alpha = -\frac{1}{4}\bar{D}^2 D_\alpha V \quad \text{(Abelian)}$$
$$W_\alpha = -\frac{1}{8g}\bar{D}^2 e^{-2gV} D_\alpha e^{2gV} \quad \text{(non-Abelian)}$$

其超对称作用量 $\int d^2\theta\, \mathrm{Tr}\, W^\alpha W_\alpha + \mathrm{h.c.}$ 在偶部给出 Yang–Mills 项、gaugino 动能项和辅助场 $D$ 项[11][15][17][18]。

### 超引力与超共形代数

若允许超对称参数依赖时空坐标（局部超对称），则天然得到**超引力**（supergravity），其中包含引力子（helicity $\pm 2$）与引力微子（gravitino，helicity $\pm\frac{3}{2}$）作为超多重态成员。**超共形代数**（superconformal algebra）进一步引入共形生成元 $D$、$K_\mu$ 与超共形生成元 $S_\alpha, \bar{S}_{\dot\alpha}$，构成包含超对称与共形对称的最大对称性代数[11][14][15]。

### 超对称 QCD 与 Seiberg 对偶

在超对称规范理论中，**超 QCD**（SQCD）展示出丰富的量子动力学行为，包括：
- **运行耦合常数与动力学尺度** Λ；
- **模空间**（moduli space）与 runaway 势；
- **Affleck–Dine–Seiberg（ADS）超势**；
- **Seiberg 对偶**：SU($N_c$) SQCD 与一个 SU($N_f - N_c$) 规范理论（**磁理论**）在红外部具有相同物理[18]。

这些现象深刻依赖于李超代数的表示论结构与 R-对称性、反常匹配（'t Hooft anomaly matching）等。

## 与超几何学的关系

李超代数是**超流形**（supermanifold）理论的核心代数结构。超流形是将普通流形的函数层 $\mathcal{O}_M$ 局部替换为
$$C^\infty(\mathbb{R}^n) \otimes \Lambda(\xi^1, \ldots, \xi^m)$$
（即在普通坐标基础上添加 $m$ 个反交换 Grassmann 生成元）所得对象[15][16]。

- **超向量场**：由超流形上的导子构成，是李超代数；
- **Frobenius 曲率**：Manin 用前 SUSY 结构（pre-SUSY structure）刻画超 Minkowski 空间：由超胚导数 $D^\alpha$ 张成的分布 $\mathcal{D}$ 是极大不可积的；
- **Berezinian**（超行列式）：与普通行列式不同，定义为
$$\mathrm{Ber}(M) = \det(A - BD^{-1}C) \det(D)^{-1}$$
（对分块矩阵 $M = \begin{pmatrix} A & B \\ C & D \end{pmatrix}$）[15][16]。

在超 Minkowski 空间 $M^{3,1|4} = \mathbb{R}^{4|4}$ 上，超对称代数的实现为向量场
$$P_\mu = \partial_\mu, \quad Q^\alpha = \frac{\partial}{\partial\theta_\alpha} + \frac{1}{4}\theta_\beta (C\gamma^\mu)^{\beta\alpha} \partial_\mu$$
其中 $C$ 为电荷共轭矩阵[15]。

## 与其他结构的联系

### 与李代数

每个李代数都可平凡地视为李超代数（取 $g_1 = 0$）。因此李超代数理论包含并推广李代数理论。

### 与 Kac–Moody 代数

反变李超代数（contragredient Lie superalgebra）由 Cartan 矩阵 $A$ 与子集 $\tau \subseteq I$ 定义：生成元 $e_i, f_i, h_i$（$i \in I$），定义关系
$$[e_i, f_j] = \delta_{ij} h_i, \quad [h_i, h_j] = 0, \quad [h_i, e_j] = a_{ij} e_j, \quad [h_i, f_j] = -a_{ij} f_j$$
其中 $i \notin \tau$ 时 $e_i, f_i$ 为偶；$i \in \tau$ 时 $e_i, f_i$ 为奇[5]。

### 与超代数/超环

李超代数是**超代数**（superalgebra）的一个特例。超代数是 $\mathbb{Z}_2$-分次代数，其中乘法满足 $A_i A_j \subseteq A_{i+j}$，与普通代数相比增加了**Koszul 符号规则**。超代数的例子包括外代数、Clifford 代数、Kähler 微分代数等[7]。

## 记号约定与文献差异

由于历史原因，不同文献在记号与符号约定上存在差异，使用时需谨慎：

- **$\mathfrak{gl}(p|q)$ 与 $\mathfrak{gl}(m|n)$**：两种记号均常见；
- **$|x|$ 与 $\bar{x}$**：奇偶性记法不统一；
- **超括号符号**：$[\cdot, \cdot]$ 与 $\{\cdot, \cdot\}$ 使用取决于元素类型；
- **Cartan 矩阵约定**：符号差（$a_{ij}$ 或 $-a_{ij}$）随文献而异；
- **R-对称性归一化**：特别是在 SQCD 等物理文献中约定多样。

## 待补充与开放问题

- **无穷维李超代数的表示论**：目前分类完备，但表示论（特别是仿射情形）仍未完全理解；
- **实李超代数的分类**：Kac 的部分结果已给出，但许多细节仍未展开；
- **与顶点算子代数（VOA）的联系**：超共形代数与 VOA 的关系仍有研究空间；
- **超 Poincaré 群的表示**：物理上广泛使用，但数学上的严格分类仍有待完善；
- **Cartan 型李超代数的有限维与无穷维关系**：正特征的类比仍未完全建立。

## 值得进一步查阅的文献

- V. G. Kac, "Lie superalgebras", *Adv. Math.* **26** (1977) 8–96（分类理论的奠基之作）；
- V. G. Kac, "A Sketch of Lie Superalgebra Theory", *Commun. Math. Phys.* **53** (1977) 31–64；
- I. M. Musson, *Lie Superalgebras and Enveloping Algebras*, Graduate Studies in Mathematics 131 (AMS, 2012)（最全面的教材之一）；
- V. S. Varadarajan, *Supersymmetry for Mathematicians: An Introduction*, Courant Lecture Notes 11 (AMS, 2004)（数学背景的物理读者入门）；
- Y. I. Manin, *Gauge Field Theory and Complex Geometry* (Springer, 2nd ed., 1997)（超几何学经典）；
- P. Deligne, J. W. Morgan, "Notes on Supersymmetry (following Joseph Bernstein)"（超线性代数系统整理）；
- Cheng & Wang, *Dualities and Representations of Lie Superalgebras*, Graduate Studies in Mathematics 144 (AMS, 2012)（表示论现代教材）。

## 参考文献

[1] Lie superalgebra, Wikipedia (en.wikipedia.org)
[2] Cheng, S.-J.; Wang, W. "Introduction", in *Dualities and Representations of Lie Superalgebras*, Graduate Studies in Mathematics 144 (AMS, 2012)
[3] Fan Zhou, "Notes on Some Basics of Lie Superalgebras" (Columbia, seminar notes)
[4] H. Boseck, "Lie Superalgebras and Lie Supergroups, I", *Seminar Sophus Lie* **1** (1991) 109–122
[5] V. G. Kac, "A Sketch of Lie Superalgebra Theory", *Commun. Math. Phys.* **53** (1977) 31–64
[6] 李超代数, 中文维基百科
[7] 超代数, 中文维基百科
[8] 李超代数, Bohrium 玻尔百科
[9] 李代数, 中文维基百科
[10] 李超代数, pkds.cc 镜像维基百科
[11] A. Maas, "Supersymmetry", Lecture Notes WS 2022/23, KFU Graz
[12] P. Deligne; J. W. Morgan, "Notes on Supersymmetry (following Joseph Bernstein)", *Quantum Fields and Strings: A Course for Mathematicians* (AMS, 1999)
[13] B. C. Allanach; F. Quevedo, "Supersymmetry", Cambridge Part III Lecture Notes (DAMTP)
[14] J. M. Figueroa-O'Farrill, "BUSSTEPP Lectures on Supersymmetry" (2001)
[15] A. J. Bruce, "A First Look at Supersymmetry", arXiv (January 2025)
[16] T. Covolo; N. Poncin, "Lectures on Supergeometry" (University of Luxembourg, 2012)
[17] D. Cassani, "Introduction to Supersymmetry", Lecture Notes (INFN Padova, July 2023)
[18] D. Tong, "Supersymmetric Field Theory", Cambridge Part III Mathematical Tripos Lecture Notes

## References

1. [Lie superalgebra](https://en.wikipedia.org/wiki/Lie_superalgebra) — en.wikipedia.org
2. [Introduction](https://www.ams.org/bookstore/pspdf/gsm-46-prev.pdf) — ams.org
3. [NOTES ON SOME BASICS OF LIE SUPERALGEBRAS Fan Zhou](https://www.math.columbia.edu/~fanzhou/files/notes_lie_superalgebras_basics.pdf) — math.columbia.edu
4. [Lie Superalgebras and Lie Supergroups, I](https://jolt.centre-mersenne.org/item/10.5802/jolt.12.pdf) — jolt.centre-mersenne.org
5. [](https://projecteuclid.org/journalArticle/Download?urlId=cmp%2F1103900590) — projecteuclid.org
6. [李超代数](https://zh.wikipedia.org/wiki/%E6%9D%8E%E8%B6%85%E4%BB%A3%E6%95%B0) — zh.wikipedia.org
7. [超代数](https://zh.wikipedia.org/wiki/%E8%B6%85%E4%BB%A3%E6%95%B0) — zh.wikipedia.org
8. [李超代数 | Bohrium](https://scipedia.bohrium.com/sciencepedia/feynman/keyword/lie_superalgebras) — scipedia.bohrium.com
9. [李代数 - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/%E6%9D%8E%E4%BB%A3%E6%95%B8) — zh.wikipedia.org
10. [李超代数 - 维基百科，自由的百科全书](https://www.pkds.cc/wikipedia/wiki/%E6%9D%8E%E8%B6%85%E4%BB%A3%E6%95%B0) — pkds.cc
11. [Supersymmetry](https://static.uni-graz.at/fileadmin/_Persoenliche_Webseite/maas_axel/susy2022-23.pdf) — static.uni-graz.at
12. [Notes on Supersymmetry (following](https://ncatlab.org/nlab/files/DeligneMorgan-NotesOnSusy.pdf) — ncatlab.org
13. [gnuplot plot](https://www.damtp.cam.ac.uk/user/examples/3P7.pdf) — damtp.cam.ac.uk
14. [](https://webhomes.maths.ed.ac.uk/~jmf/Teaching/Lectures/BUSSTEPP.pdf) — webhomes.maths.ed.ac.uk
15. [A First Look at Supersymmetry](https://arxiv.org/html/2412.07799v2) — arxiv.org
16. [Lectures on Supergeometry](https://orbilu.uni.lu/bitstream/10993/14295/1/LecturesSupergeometryFinalRevised.pdf) — orbilu.uni.lu
17. [Introduction to Supersymmetry](https://userswww.pd.infn.it/~cassani/susy_lecture_notes.pdf) — userswww.pd.infn.it
18. [Supersymmetric Field Theory](https://davidtong.org/pdfs/teaching/supersymmetric-field-theory/susy.pdf) — davidtong.org
