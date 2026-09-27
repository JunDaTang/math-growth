---
type: query
title: "Research: 一元泰勒定理（带 Lagrange 余项）尚未入库"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 一元泰勒定理（带 Lagrange 余项）尚未入库

# 一元泰勒定理（带 Lagrange 余项）

## 摘要

一元泰勒定理是微分学的核心逼近定理：若函数在某点 $a$ 附近足够光滑，则可用 $a$ 处各阶导数构成的 $n$ 次泰勒多项式逼近函数值，逼近误差由**拉格朗日（Lagrange）余项**刻画。该定理被视为拉格朗日中值定理的高阶推广，也是泰勒级数收敛性、解析函数理论（与 [[柯西定理解析解]]、[[解析延拓]]、[[收敛圆]] 相关）以及各类数值误差估计的出发点。

本页综合多份英文与中文资料，梳理定理的严格陈述、若干余项形式、三条主要证明路径、误差界、历史脉络，并标注了资料之间的细微分歧与尚待补充之处。

---

## 1. 定理陈述

设 $n$ 是正整数。若定义在包含点 $a$ 的区间上的函数 $f$ 在 $a$ 处（或该区间上）$n+1$ 次可导，则对该区间内任意 $x$，有 [6][10][12]

$$
f(x)=f(a)+\frac{f'(a)}{1!}(x-a)+\frac{f^{(2)}(a)}{2!}(x-a)^{2}+\cdots+\frac{f^{(n)}(a)}{n!}(x-a)^{n}+R_n(x),
$$

其中 $R_n(x)$ 称为泰勒公式的**余项**，是 $(x-a)^n$ 的高阶无穷小；若取**拉格朗日型余项**，则

$$
R_n(x)=\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-a)^{n+1},\qquad \xi \text{ 介于 } a \text{ 与 } x \text{ 之间.}
$$

该余项中的 $\xi$ 由中值定理保证存在，但**一般不可求**；实际问题通常只求其上界 [9][13]。mathwords 特别指出一个易错点：度为 $n$ 的多项式之后，余项**总是**含有第 $(n+1)$ 阶导数、$(x-a)$ 的 $(n+1)$ 次幂与 $(n+1)!$，可记作「多项式之外的下一个项」[13]。

> **注（零阶退化）**：当 $n=0$ 时，公式退化为 $f(x)-f(a)=f'(\xi)(x-a)$，即拉格朗日中值定理 [6][2]。因此中文资料常称「带拉格朗日型余项的泰勒公式可视为拉格朗日微分中值定理的推广」[6]。这一点在第 8 节另有更细致的辨析。

---

## 2. 余项的其他形式（对照）

余项有多种命名形式，不同形式适用的条件与用途不同：

| 余项形式 | 表达式 | 特点 |
|---|---|---|
| Peano（佩亚诺）余项 | $R_n(x)=o[(x-a)^n]$ | 仅需 $a$ 处前 $n$ 阶导数，适用于局部极限估计 [6][10] |
| Lagrange（拉格朗日）余项 | $R_n(x)=\dfrac{f^{(n+1)}(\xi)}{(n+1)!}(x-a)^{n+1}$ | 给出具体误差范围，中值定理型 [6][13] |
| Cauchy（柯西）余项 | 由引理 2 取参数得到 | 同样给出具体误差范围 [10] |
| 积分型余项 | $R_n(x)=\displaystyle\int_a^x \frac{f^{(n+1)}(t)}{n!}(x-t)^{n}\,dt$ | 可视为微积分基本定理的推广，靠牛顿–莱布尼茨公式导出 [6][10] |
| 迭代/多重积分余项 | $R_{n+1}(x)=\displaystyle\int_a^x\!\!\int_a^{x_1}\!\!\cdots\!\!\int_a^{x_n} f^{(n+1)}(x_{n+1})\,dx_{n+1}\cdots dx_1$ | 反复积分反复「塞入」$a$ 处信息，余项形式较繁 [1] |

Brilliant 的资料把最后一种形式当作主定义，并说明该形式在多元微积分中常见，「这或许正是泰勒定理很少以这种方式讲授的原因」[1]。百度百科则把佩亚诺余项定位为局部估计、拉格朗日与柯西余项定位为可给出误差范围、积分型余项定位为牛顿–莱布尼茨公式的推广 [10]。

---

## 3. 三条主要证明路径

### 3.1 迭代积分法

从微积分基本定理出发，把 $f(x)$ 表为

$$
f(x)=f(a)+\int_a^x f'(x_1)\,dx_1,
$$

再对 $f'(x_1)$ 在 $a$ 处重复展开，即得二阶项加一个二重积分；如此迭代 $n$ 次，得到「$a$ 处的 $n$ 次泰勒多项式 + 一个 $n+1$ 重积分」的形式 [1]。利用 Fubini 定理可调整积分次序使内层积分更易计算 [1]。

**算例（Brilliant）**：对 $f(x)=\sin x$、$a=0$、$n=3$，直接计算

$$
R_4(x)=\int_0^x\!\!\int_0^{x_1}\!\!\int_0^{x_2}\!\!\int_0^{x_3}\sin x_4\,dx_4\,dx_3\,dx_2\,dx_1=\frac{x^3}{3!}-x+\sin x,
$$

恰好验证了 $\sin x$ 的三阶泰勒展开 [1]。

### 3.2 积分型余项 + 积分第一中值定理（较弱版本）

百度百科给出一个更「自然」但**条件更强**的证明：若 $f$ 及其前 $n+1$ 阶导数在 $[x_0,x]$ 上连续，考虑积分型余项

$$
R_n(x)=\int_{x_0}^{x}\frac{f^{(n+1)}(t)}{n!}(x-t)^{n}\,dt,
$$

由于被积函数中 $t\mapsto (x-t)^n$ 在 $[x_0,x]$ 上不变号、$f^{(n+1)}$ 连续，由**积分第一中值定理**存在 $\xi$ 使

$$
R_n(x)=\frac{f^{(n+1)}(\xi)}{n!}\int_{x_0}^{x}(x-t)^{n}\,dt=\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1},
$$

即得拉格朗日余项 [10]。文献明确指出这是「较弱的拉格朗日余项」，因为额外要求了 $f$ 的 $n+1$ 阶导数连续（称「较弱」）[10]。

### 3.3 高阶罗尔定理 + 柯西中值定理（标准证明）

Gowers 的博客给出一个广泛流传的证明，其思路与 C. H. Edwards 所著《Advanced Calculus of Several Variables》中的证明「几乎完全相同」：引入**高阶罗尔定理**，再配合（柯西型）中值定理得到拉格朗日余项 [2]。

CSDN 上的一篇笔记同样以「用柯西定理证明泰勒公式的拉格朗日余项」为题 [8]，与百度百科的**引理 2** 路线一致：引理 2 通过**柯西中值定理**证明，在其中分别取不同的参数即可依次得到**柯西余项**与**拉格朗日余项**公式 [10]。Gowers 亦强调，该路线相较积分法能摆脱对高阶导数连续性的过度要求（其批评 Edwards 未处理 Peano 形式，因而「在不该假设的地方假设了过多可微性」）[2]。

### 3.4 与中值定理的深层关系

Gowers 用一个更「对称」的定理来概括问题：设 $f$ 在区间上连续、在包含该区间的开区间内 $n$ 次可导，$p$ 是满足 $p^{(k)}(x)=f^{(k)}(x)\ (k=0,\dots,n-1)$ 且 $p(x+h)=f(x+h)$ 的唯一 $n$ 次多项式，则存在 $\theta\in(0,1)$ 使 $f^{(n)}(x+\theta h)=p^{(n)}(x+\theta h)$ [2]。当 $n=1$ 时，$p^{(1)}$ 为常值 $(f(x+h)-f(x))/h$，定理即退化为拉格朗日中值定理 [2]。

---

## 4. 误差估计（Lagrange 误差界 / Taylor 不等式）

实际计算中更常用的是余项的**上界**而非其精确值。常见表述：

**Taylor 不等式**：若 $f$ 在包含 $a$ 与 $x$ 的区间上有 $n+1$ 阶连续导数，且对 $a$ 与 $x$ 之间的所有 $t$ 有 $|f^{(n+1)}(t)|\le M_{n+1}$，则

$$
|R_n(x)|\le \frac{M_{n+1}}{(n+1)!}\,|x-a|^{n+1}. \tag{1}
$$

[11]

Khan Academy 的「Lagrange 误差界」（又称 Taylor's Remainder Theorem）用略有不同的措辞给出同一结论：若 $|f^{(n+1)}|\le M$ 在含中心与 $x$ 的开区间上成立，则可据此确定所需的泰勒多项式次数，使误差小于给定界；视频以 $\sin(0.4)$ 为例演示 [4]。mathwords 也强调正确做法是**求导数的上界**而非试图求出 $c$ 的精确值 [13]。

**文献中的算例**：

- 用零心二阶泰勒多项式估计 $\cos(0.6)$，由 $|{\sin c}|\le 1$ 得误差 $\le \dfrac{1}{3!}|x|^3\big|_{x=0.6}=0.036$ [12]。
- 用三阶多项式 $\sin x\approx x-\dfrac{x^3}{6}$，要求误差不超过 $4\times 10^{-3}$，解得 $|x|\le \sqrt[4]{4!\cdot 0.004}\approx 0.556$ [12]。
- 用零心三阶多项式估计 $e^{0.5}$，取 $e^{0.5}<2$，得 $|R_3(0.5)|\le \dfrac{2}{4!}(0.5)^4\approx 0.00521$ [13]。
- YouTube 算例：对 $\sqrt{1.2}$ 取 $n=2$、$a=1$，计算第三阶导数并给出最大误差估计 [15]（该转录的数值呈现为「5/104」，与按 (1) 式手算的结果量级不符，疑为转录讹误，见第 9 节）。

---

## 5. 最佳逼近性质

华盛顿大学讲义给出了一个重要的**唯一性/最优性**刻画：在一切 $n$ 次多项式中，泰勒多项式 $T_n(x)$ 是**唯一**满足

$$
f(x)-T_n(x)=O\big(|x-a|^{n+1}\big)
$$

者；任何其他 $n$ 次多项式与 $f(x)$ 的偏差至少是常数倍的 $|x-a|^{n}$，比泰勒多项式差一个 $|x-a|$ 因子。这解释了为什么称 $T_n(x)$ 为在 $a$ 附近「最佳拟合」$f(x)$ 的 $n$ 次多项式 [11]。

---

## 6. 历史脉络

- **1671**：格雷戈里（Gregory）已发现泰勒公式的某个特例；其前身可追溯到**格雷戈里–牛顿插值公式** [10]。
- **1712**：泰勒（Brook Taylor）在给老师梅钦（John Machin）的信中首次完整陈述该公式 [10]。
- **1715**：泰勒在《正的和反的增量方法》（*Methodus Incrementorum Directa et Inversa*）中正式发表 [10]。
- **1717**：泰勒用该公式求解数值方程 [10]。
- **1772**：拉格朗日强调泰勒公式的重要性，称其为**微分学基本定理**，并提出带余项的现代形式；但其证明尚未考虑级数收敛性 [10]。
- **19 世纪 20 年代**：柯西完成收敛性的严格证明，定理方得完备 [10]。此线亦与 [[柯西]] 在解析解理论中的工作相呼应（参见 [[柯西定理解析解]]）。

zh.wikipedia 转引的参考文献包括 O'Connor 与 Robertson 的 Brook Taylor 传记、Rudin《数学分析原理》第 123–124 页、Klein (1998) 20.3、Apostol (1967) 7.7 以及 Protter 与 Morrey 第 135–136 页 [6]，可作为进一步核实的线索。

---

## 7. 与级数的衔接

- 泰勒定理可用于**严格论证函数的幂级数展开**：Gowers 以 $\sin x$ 为例，指出在未证明「幂级数可逐项求导」之前，不能直接断言 $\sin x$ 等于其幂级数；应用泰勒定理（$x\to 0$、$h\to x$）后得

$$
\sin x=\underbrace{\sum_{k=0}^{n-1}\frac{\sin^{(k)}(0)}{k!}x^k}_{\text{部分和}}+\ \text{余项},
$$

遂可据此处理 [2]。这与 [[复数项级数]]、[[收敛圆]] 及复分析中解析函数的级数表示直接相关。
- 百度百科提醒：并非每个无穷阶可微函数的泰勒级数都在某个邻域收敛；即便收敛，也未必收敛到生成它的函数——只有**解析函数**才保证在 $x_0$ 的某邻域内泰勒级数收敛到原函数 [10]。这正是 [[解析延拓]] 与全纯函数理论的出发点。
- **多元推广**：对 $f(a+h)$，上式可写作 $f(a)+Jf(a)h+\frac12 h^\top Hf(a)h+\cdots$，其中 $Jf$ 为雅可比矩阵、$Hf$ 为海森矩阵 [6]。

---

## 8. 争议与细微之处

1. **拉格朗日余项是否依赖拉格朗日中值定理？** 主流中文资料称带拉格朗日余项的泰勒公式是拉格朗日中值定理的推广 [6]。但一篇知乎文章提出不同看法：拉格朗日余项**并不依赖**拉格朗日中值定理，其底层依据是比中值定理更基本的**连续函数介值定理**；该余项「只在零阶近似时恰好等于拉格朗日中值」，故「推广」之说并不精确 [7]。这一分歧本质上是证明路径选择（介值/罗尔/柯西中值）的差异，建议在教学中区分「形式上的退化」与「证明上的依赖」。

2. **「较弱」与「较强」版本的假设差异。** 积分法给出的版本在额外要求 $n+1$ 阶导数连续时成立 [10]，而引理 2 路线（柯西中值定理）可放宽该假设 [2][10]。Gowers 亦批评 Edwards 未处理 Peano 形式，导致「在不该假设的地方假设了过多可微性」[2]。

3. **余项的「下一个项」直觉虽好，但不能当精确值。** 资料反复提醒 $\xi$（或 $c$）未知，只能求上界 [9][13]；拉格朗日余项定理与中值定理、介值定理一样属于**存在性定理**，只能断言值存在而不能给出具体点 [9]。

4. **高阶罗尔定理中的下标笔误。** 在 Gowers 博文的评论中，Tom Leinster 指出「A higher order Rolle theorem」第二段首句有笔误，$n$ 应为 $n-1$ [2]，阅读原文时需注意。

---

## 9. 缺口与待考证

- **Peano 余项的严格证明细节缺失。** 现有资料多给出 Peano 余项的结论式而略去其证明（Gowers 明确指出 Edwards 未处理该形式）[2]。
- **$n$ 与 $n+1$ 的下标约定不统一。** 不同资料对「$R_n$ 含第 $n+1$ 阶导数」还是「$R_{n+1}$ 含第 $n+1$ 阶导数」写法不一 [1][6][12]，跨源引用时需格外小心。
- **弱版本的「连续」假设是否必要**，各源表述不完全一致（[10] 要求 $[x_0,x]$ 上连续，[11][12] 要求 $n+1$ 阶连续导数），尚缺统一的必要/充分条件对照。
- **视频转录的数值误差。** [15] 中 $\sqrt{1.2}$ 的误差结果在文字转录里呈现为「5/104」，与按 (1) 式手算（$\frac{3}{8}\cdot\frac{(0.2)^3}{3!}=\frac{1}{2000}$）不符，疑为自动字幕对「1/2000」的识别讹误，需回看原视频核实。
- **复分析方向未展开。** 本页所据英文资料主要面向实变量一元微积分；复变量情形（解析函数的泰勒级数、[[解析延拓]]、[[收敛圆]]）应结合已有的复分析条目补全。
- **与本 wiki 已有条目的衔接点尚未建立**，如 [[柯西定理解析解]]（解析解幂级数）、[[广义导数]]（积分型余项在弱可微下的推广）之间缺少显式链接与对照。

---

## 10. 建议补充的文献

1. **Rudin，《数学分析原理》**（转引自 [6]，第 123–124 页）——拉格朗日余项的标准严格证明。
2. **Apostol, *Mathematical Analysis* (1967) 7.7；Klein (1998) 20.3；Protter & Morrey, pp. 135–136**（转引自 [6]）——不同证明路径与历史注记。
3. **C. H. Edwards, *Advanced Calculus of Several Variables***（经 [2] 转述）——高阶罗尔定理 + 柯西中值定理路线的原始出处。
4. **O'Connor & Robertson, «Brook Taylor's Biography»**（转引自 [6]）——历史细节核实。
5. 关于**佩亚诺余项**与**弱可微条件下**的余项推广（关联 [[广义导数]]、[[索伯列夫空间]]）。
6. 关于**解析函数泰勒级数收敛性**的复分析教材章节（关联 [[收敛圆]]、[[解析延拓]]）。

---

## 参考文献

[1] Brilliant Math & Science Wiki, *Taylor's Theorem (with Lagrange Remainder)*. [2] Gowers's Weblog, *Taylor's theorem with the Lagrange form of the remainder*. [3] Math StackExchange, *Intuition behind Lagrange remainder term in Taylor's theorem*. [4] Khan Academy, *Worked example: estimating sin(0.4) using Lagrange error bound*. [5] Reddit, *[Calculus] Lagrange error bound for Taylor polynomials*. [6] 维基百科（中文），「泰勒公式」。 [7] 知乎，〈泰勒公式终极理解，真正从 0 发明泰勒〉。 [8] CSDN，〈用柯西定理证明泰勒公式的拉格朗日余项〉。 [9] surprisedcat.github.io，〈数学分析之拉格朗日余项与误差〉。 [10] 百度百科，「泰勒公式」。 [11] University of Washington, *Taylor Polynomials and Taylor Series* (讲义 PDF)。 [12] people.math.sc.edu, *Estimation of the Taylor Remainder*。 [13] Mathwords, *Taylor Series Remainder: Lagrange Form $R_n(x)$*。 [14] Khan Academy, *Taylor polynomial remainder (part 1)*（视频）。 [15] YouTube, *Taylor's Remainder Theorem*（核算例视频）。

## References

1. [Taylor's Theorem (with Lagrange Remainder) | Brilliant Math & Science Wiki](https://brilliant.org/wiki/taylors-theorem-with-lagrange-remainder) — brilliant.org
2. [Taylor’s theorem with the Lagrange form of the remainder | Gowers's Weblog](https://gowers.wordpress.com/2014/02/11/taylors-theorem-with-the-lagrange-form-of-the-remainder) — gowers.wordpress.com
3. [Intuition behind Lagrange remainder term in Taylor's ...](https://math.stackexchange.com/questions/4456518/intuition-behind-lagrange-remainder-term-in-taylors-theorem) — math.stackexchange.com
4. [Worked example: estimating sin(0.4) using Lagrange error bound (video) | Khan Academy](https://www.khanacademy.org/math/ap-calculus-bc/bc-series-new/bc-10-12/v/lagrange-error-bound-for-sine-function) — khanacademy.org
5. [[Calculus] Lagrange error bound for Taylor polynomials](https://www.reddit.com/r/learnmath/comments/7q6i3h/calculus_lagrange_error_bound_for_taylor) — reddit.com
6. [泰勒公式 - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/%E6%B3%B0%E5%8B%92%E5%85%AC%E5%BC%8F) — zh.wikipedia.org
7. [泰勒公式终极理解, 真正从0发明泰勒 ...](https://zhuanlan.zhihu.com/p/355819201) — zhuanlan.zhihu.com
8. [用柯西定理证明泰勒公式的拉格朗日余项](https://blog.csdn.net/weixin_43873202/article/details/115425427) — blog.csdn.net
9. [数学分析之拉格朗日余项与误差](https://surprisedcat.github.io/studynotes/%E6%95%B0%E5%AD%A6%E5%88%86%E6%9E%90%E4%B9%8B%E6%8B%89%E6%A0%BC%E6%9C%97%E6%97%A5%E4%BD%99%E9%A1%B9%E4%B8%8E%E8%AF%AF%E5%B7%AE) — surprisedcat.github.io
10. [泰勒公式](https://baike.baidu.com/item/%E6%B3%B0%E5%8B%92%E5%85%AC%E5%BC%8F/7681487) — baike.baidu.com
11. [[PDF] Taylor Polynomials and Taylor Series](https://math.washington.edu/~perkins/126EAut14/Taylor_Polynomials.pdf) — math.washington.edu
12. [Estimation of the Taylor Remainder](https://people.math.sc.edu/josephcf/Teaching/142/Files/Worksheets/Estimation%20of%20the%20Taylor%20Remainder.pdf) — people.math.sc.edu
13. [Taylor Series Remainder: Lagrange Form Rₙ(x)](https://www.mathwords.com/t/taylor_series_remainder.htm) — mathwords.com
14. [Taylor polynomial remainder (part 1) (video) | Khan Academy](https://www.khanacademy.org/math/ap-calculus-bc/bc-series-new/bc-10-12/v/error-or-remainder-of-a-taylor-polynomial-approximation) — khanacademy.org
15. [Taylor's Remainder Theorem](https://www.youtube.com/watch?v=lY0LzJXTgeo) — youtube.com
