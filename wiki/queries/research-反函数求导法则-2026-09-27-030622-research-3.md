---
type: query
title: "Research: 反函数求导法则"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 反函数求导法则

# 反函数求导法则

**反函数求导法则**（英语：inverse function rule；单变量情形亦常称反函数求导公式）是微积分中刻画一对互逆函数之导数关系的基本公式。它断言：在适当条件下，反函数在某点的导数等于原函数在对应点（即该点的原像，英文来源 [1] 称之为 *correlate*）处导数的倒数 [1][2][3][11]。多变量及向量值情形下的推广称为"反函数定理"（inverse function theorem），其结论由导数（雅可比矩阵）的求逆给出 [5][7]。

本页综合 Math Vault、OpenStax/LibreTexts、英语与中文维基百科、Khan Academy 等来源，梳理该法则的陈述、证明、几何意义、典型应用、多变量推广以及若干记法与条件上的疑义。

---

## 1. 定理陈述（单变量情形）

设 $f$ 在区间 $I$ 上单射（因而其反函数 $f^{-1}$ 定义于 $f(I)$ 上）。若 $f$ 在点 $f^{-1}(y)$ 处可导，且

$$f'\big(f^{-1}(y)\big) \neq 0,$$

则 $f^{-1}$ 在 $y$ 处可导，并且

$$\big(f^{-1}\big)'(y)=\frac{1}{f'\big(f^{-1}(y)\big)}. \tag{1}$$

[2][3][11]

若改用另一记法，设 $y=g(x)$ 是 $f(x)$ 的反函数，则等价地有

$$g'(x)=\frac{1}{f'\big(g(x)\big)}. \tag{2}$$

[2][3]

在 Leibniz 记号下，该法则亦可写成两条微分之比的互逆形式：

$$\frac{dx}{dy}\,\frac{dy}{dx}=1. \tag{3}$$

[11]

与原函数单射性相关的存在性问题，参见 [[反函数存在性所需条件]] 与 [[反函数]]。

---

## 2. 证明

### 2.1 由反函数恒等式配合链式法则

最直接的推导只用反函数的基本性质

$$x=f\big(f^{-1}(x)\big).$$

将等式两边对 $x$ 求导，右端对复合函数使用链式法则，得

$$1=f'\big(f^{-1}(x)\big)\cdot \big(f^{-1}\big)'(x).$$

解出 $\big(f^{-1}\big)'(x)$ 即得式 (1) [2][3]。

### 2.2 Leibniz 记号的推导

从 $f^{-1}(y)=x$ 出发，对 $x$ 求导并同样运用链式法则，可得

$$\frac{dx}{dy}\,\frac{dy}{dx}=\frac{dx}{dx}=1,$$

因为 $x$ 对自身的导数为 1 [11]。这一写法直观地表达了"斜率互为倒数"的思想。

### 2.3 几何直觉与定理背景

来源 [1] 强调，单变量反函数求导法则的几何直觉正是数学分析中"反函数定理"的骨干：函数与其反函数的图像关于直线 $y=x$ 互为镜像，因此对应点处切线斜率互为倒数。这一几何事实在曲线层面相当于 [[反三角函数图像的对角线反射]] 所描述的对角线反射现象。来源 [1] 还指出，该结论"无需借助任何更高深的数学工具"即可得到。

---

## 3. 典型应用

### 3.1 对数函数（欧拉 $e$ 函数之反函数）

以自然底 $e$ 为例，指数函数 $f(x)=e^{x}$（定义于 $\mathbb{R}$）的反函数是 $\ln x$（定义于 $\mathbb{R}_{+}$）。按式 (1) 的三个步骤计算 $\ln x$ 在 $x>0$ 处的导数 [1]：

1. **原像**：$f^{-1}(x)=\ln x$；
2. **原函数在原像处的导数**：$\big[e^{x}\big]_{x=\ln x}=e^{\ln x}=x$；
3. **取倒数**：$\dfrac{1}{x}$。

于是 $(\ln x)'=\dfrac{1}{x}$（$x>0$）[1]。相关的函数方程刻画与反函数结构参见 [[欧拉e函数]] 与 [[指数函数与对数的函数方程]]。

### 3.2 反三角函数

来源 [2]（OpenStax/LibreTexts 教材所列"Key Equations"）在该法则下集中列出了六个反三角函数的导数：

$$\frac{d}{dx}\sin^{-1}x=\frac{1}{\sqrt{1-x^{2}}},\quad \frac{d}{dx}\cos^{-1}x=\frac{-1}{\sqrt{1-x^{2}}},$$
$$\frac{d}{dx}\tan^{-1}x=\frac{1}{1+x^{2}},\quad \frac{d}{dx}\cot^{-1}x=\frac{-1}{1+x^{2}},$$
$$\frac{d}{dx}\sec^{-1}x=\frac{1}{|x|\sqrt{x^{2}-1}},\quad \frac{d}{dx}\csc^{-1}x=\frac{-1}{|x|\sqrt{x^{2}-1}}.$$

这些结果正是把 [[queries/research-反函数求导法则-2026-09-27-030622-research-3]] 应用于 [[正弦余弦的导数]] 等已知导数后取倒数的产物；本 wiki 已将其系统整理于 [[反三角函数的导数]]，并有 [[反三角函数的主值区间]] 说明定义域分支的选择，以及 [[反三角函数的导数为代数函数]] 说明其结果仍属代数函数。

### 3.3 数值例题

**直接验证**：设 $g(x)=\dfrac{x+2}{x}$，其反函数为 $f(x)=\dfrac{2}{x-1}$。由式 (2) 先算

$$f'(x)=\frac{-2}{(x-1)^{2}},\qquad f'\big(g(x)\big)=\frac{-2}{\left(\frac{x+2}{x}-1\right)^{2}}=-\frac{x^{2}}{2},$$

故

$$g'(x)=\frac{1}{f'\big(g(x)\big)}=-\frac{2}{x^{2}},$$

与直接对 $g$ 求导所得一致 [2][3]。

**Khan Academy 例题**：已知 $H$ 是 $F$ 的反函数，且 $F(-2)=-14$，求 $H'(-14)$。此题即按"求原像 → 算原函数在该点导数 → 取倒数"三步完成，若无该法则会显得相当困难 [8]。

---

## 4. 多变量推广：反函数定理

在数学分析中，反函数定理（英语：inverse function theorem）给出向量值函数在其定义域内一点的开区域内存在反函数的充分条件；对满足条件的函数，定理断言反函数的全导数存在，并给出计算公式 [5][7]。

**陈述**（有限维）：若从 $\mathbb{R}^{n}$ 的开集 $U$ 到 $\mathbb{R}^{n}$ 的连续可微函数 $F$ 在点 $p$ 处全微分可逆（即雅可比行列式 $\det J_{F}(p)\neq 0$），则 $F$ 在 $p$ 的某邻域内存在反函数，且 $F^{-1}$ 亦连续可微，并有

$$J_{F^{-1}}\big(F(p)\big)=\big[J_{F}(p)\big]^{-1}, \tag{4}$$

其中 $J_{G}(q)$ 表示 $G$ 在 $q$ 处的雅可比矩阵 [7]。

**公式与链式法则的关系**：式 (4) 也可由链式法则推出。设 $G=F$、$H=F^{-1}$，则 $G\circ H$ 为恒等映射，其雅可比矩阵为单位矩阵，于是可从中解出 $J_{F^{-1}}$。来源 [7] 特别指出：链式法则假定了 $H$ 的全导数存在，而反函数定理则进一步**证明**了 $F^{-1}$ 在相应点具有全导数。

**例子**：对 $\mathbf{F}(x,y)=\begin{bmatrix}e^{x}\cos y\\ e^{x}\sin y\end{bmatrix}$，其雅可比行列式为 $\det J_{F}(x,y)=e^{2x}$，处处不为零，故 $\mathbb{R}^{2}$ 中任一点附近 $F$ 都存在反函数 [7]。

### 4.1 证明方法

- **压缩映射原理（巴拿赫不动点定理）**：教科书中最常见的证明，也可用于证明无穷维（巴拿赫空间）情形；该定理还可用于证明常微分方程解的存在唯一性 [7][15]。
- **紧集上函数的极值定理**：仅适用于有限维情形 [7]。
- **牛顿法**：给出定理的一种有效形式，即在给定导数界的前提下可估计可逆邻域的大小 [7]。
- **Spivak 路线**：来源 [13] 明确标注其证明"主要借自 Spivak 的 *Calculus on Manifolds*"。
- **泰勒截断与压缩**：来源 [15]（Terry Tao）给出标准证明细节——把 $x_0=f(x_0)=0$ 与 $Df(0)$ 规范化，利用 $Df$ 的连续性和微积分基本定理使 $x\mapsto x-f(x)+y$ 在小球上成为压缩映射，再由压缩映射定理完成证明。

### 4.2 复变与无穷维情形

- **复变情形**：来源 [14] 给出推论——若 $G\subset\mathbb{C}$ 开、$f$ 在 $G$ 上全纯且 $f'(z_0)\neq 0$，则存在开集 $U,V$ 使 $f:U\to V$ 为一对一满射，且 $f^{-1}$ 全纯。其证明把 $G$ 视作 $\mathbb{R}^2$ 的开子集，并利用 $\det DF(x_0,y_0)=|f'(z_0)|^{2}\neq 0$ [14]。
- **无穷维**：定理可推广到巴拿赫空间及巴拿赫流形，需要弗雷歇导数在 $p$ 附近具有有界反函数 [7]。
- **流形与常秩定理**：反函数定理可推广到可微流形之间的可微映射，并与常秩定理相联系 [7]。
- **弱化连续可微性**：来源 [15] 指出，标准证明所用的"连续可微"假设可放宽为"处处可导"。

---

## 5. 条件、记法与相关讨论

- **非零导数条件**：式 (1) 中 $f'\big(f^{-1}(y)\big)\neq 0$ 是本质性的。当原函数在对应点导数为零时，其反函数在该点通常不可导（或导数趋于无穷），因此各来源均显式标出该条件 [2][3][11]。来源 [1] 的表述是"当 $\frac{1}{f'(f^{-1}(x))}$ 有意义时"。
- **可导性假设的位置**：来源 [1] 只说"若该表达式有意义"，而 [2][3][11] 额外要求 $f$ 在原像处可导。二者实质一致，但严格性略有差别——这属于表述层面的细微差异，而非矛盾。
- **变量记法的差异**：来源 [2][3] 以 $x$ 为反函数自变量（$\big(f^{-1}\big)'(x)=\cdots$），来源 [11] 以 $y$ 为反函数自变量（$\left[f^{-1}\right]'(y)=\cdots$）。二者仅符号选择不同，公式本身一致。维基百科 [11] 采用 Lagrange 记法并另给 Leibniz 记法。
- **"反函数求导法则"与"反函数定理"的命名**：英语维基百科将初等单变量公式单列为 *Inverse function rule*（[11]），而将多变量情形单列为 *Inverse function theorem*。中文维基百科的"反函数定理"条目 [5][7] 则主要讨论多变量、向量值情形。这提示中文语境中"反函数求导法则"（初等单变量）与"反函数定理"（多变量/分析）宜区分对待——详见下节开放问题。

---

## 6. 矛盾、空白与开放问题

1. **条目命名的层次区分**：目前收集到的中文来源（[[10-数学指南实用数学手册--10-0212-反三角函数--1g1n0g5]] 所涉教材体系、百度百科 [10]、中文维基 [5][7]）倾向于把"反函数"的定义、单变量求导公式与多变量反函数定理混在同一命名下。是否需要像英语维基那样，将**单变量求导法则**与**多变量反函数定理**拆分为两个独立条目，值得进一步厘清。
2. **证明细节不完整**：压缩映射路线与 Spivak 路线在 [13][14][15] 中仅给出梗概或片段，本 wiki 尚未整理出一份自洽、逐步的完整证明。若要作为独立"证明"页面，仍需补足对 $\|\cdot\|$ 估计、规范化 $Df(0)=I$、开集/连通性论证等环节 [15]。
3. **$f'\neq 0$ 的反例**：收集到的来源中未见针对"$f'(f^{-1}(y))=0$ 时反函数不可导"的具体反例（如 $f(x)=x^{3}$ 在 $x=0$ 处的情形）。这属于内容空白。
4. **连续可微假设的最弱形式**：来源 [15] 提到可弱化为"处处可导"，但其证明依赖较深的拓扑论证（有限交性质、连通分支分离等），尚未在本 wiki 中系统化。

---

## 7. 建议补充的来源

- Spivak, *Calculus on Manifolds*（来源 [13] 已直接征引，可补入原书条目）。
- Rudin, *Principles of Mathematical Analysis*；Apostol, *Mathematical Analysis*（多变量反函数定理的标准证明）。
- Krantz & Parks, *The Implicit Function Theorem: History, Theory, and Applications*（反函数定理与隐函数定理的历史与等价性）。
- OpenStax *Calculus* 第 3.7 节原文（来源 [2][3] 的完整出处，可核对"Key Equations"与例题细节）。
- 关于"单变量反函数求导法则"与"多变量反函数定理"命名分立的语言/教材比较资料。

---

## 相关条目

- [[反函数]]
- [[反函数存在性所需条件]]
- [[反三角函数的导数]]
- [[反三角函数的主值区间]]
- [[反三角函数图像的对角线反射]]
- [[反三角函数的导数为代数函数]]
- [[正弦余弦的导数]]
- [[欧拉e函数]]
- [[指数函数与对数的函数方程]]
- [[函数的单调性]]

## References

1. [Derivative of Inverse Functions: Theory and Applications | Math Vault](https://mathvault.ca/derivative-inverse-functions) — mathvault.ca
2. [Derivatives of Inverse Functions](https://www2.math.uconn.edu/ClassHomePages/Math1071/Textbook/sec_Ch3Sec7.html) — www2.math.uconn.edu
3. [3.7: Derivatives of Inverse Functions - Mathematics LibreTexts](https://math.libretexts.org/Bookshelves/Calculus/Calculus_(OpenStax)/03%3A_Derivatives/3.07%3A_Derivatives_of_Inverse_Functions) — math.libretexts.org
5. [反函数定理 - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/反函数定理) — zh.wikipedia.org
7. [反函数定理 - 维基百科，自由的百科全书](https://zh.wikipedia.org/wiki/%E5%8F%8D%E5%87%BD%E6%95%B0%E5%AE%9A%E7%90%86) — zh.wikipedia.org
8. [反函数求导：从方程式中(视频)](https://zh.khanacademy.org/math/differential-calculus/dc-chain/dc-inverse-func-diff/v/derivatives-of-inverse-functions-implicit) — zh.khanacademy.org
10. [反函数](https://baike.baidu.com/item/%E5%8F%8D%E5%87%BD%E6%95%B0/91388) — baike.baidu.com
11. [Inverse function rule - Wikipedia](https://en.wikipedia.org/wiki/Inverse_function_rule) — en.wikipedia.org
13. [The Inverse Function Theorem](https://mathweb.ucsd.edu/~nwallach/inverse[1].pdf) — mathweb.ucsd.edu
14. [a proof of the inverse function theorem](https://people.math.sc.edu/schep/InversefunctionThm.pdf) — people.math.sc.edu
15. [The inverse function theorem for everywhere differentiable maps | What's new](https://terrytao.wordpress.com/2011/09/12/the-inverse-function-theorem-for-everywhere-differentiable-maps) — terrytao.wordpress.com

## Related
- [[queries/research-补充链式法则的标准证明-2026-09-27-073900-research-53]]
- [[queries/research-雅可比行列式jacobi-行列式-2026-09-27-042944-research-35]]
