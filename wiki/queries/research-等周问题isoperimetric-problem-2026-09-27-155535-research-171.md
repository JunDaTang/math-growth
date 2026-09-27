---
type: query
title: "Research: 等周问题（isoperimetric problem）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 等周问题（isoperimetric problem）

# 等周问题（isoperimetric problem）

等周问题是变分法与几何分析中最古老、最经典的极值问题：在周长（或弧长）固定的条件下，寻找使所围面积最大的图形；其解为圆（在带直线边界的情形下为半圆）。该问题在文献中既被称作**等周问题**，也被表述为**等周定理**或**等周不等式**（isoperimetric inequality）[8][10]。它是变分法（calculus of variations）的入门范例，也是检验带约束极值方法（尤其是 Lagrange 乘子与 Euler–Lagrange 方程）的标准例题[4][9][12]。

## 1. 历史渊源：Dido 传说

等周问题在数学文献中通常以「Dido 问题」（Dido's problem）之名出现。按流传的叙述，它源于古代文学中的一则神话（与迦太基的建立传说相关），后来从「神话」转化为一个严格的数学问题[1]。来源 [9] 即以「一个爱情悲剧里的数学问题」为题介绍该问题的数学内容。

从神话到数学问题的转变，构成了该主题的一条独立研究线索：来源 [1]（arXiv）的标题正指向「古代文学中的神话如何成为一个数学问题」这一过程。由于本条目的检索材料多为摘要或片段，神话细节（如「牛皮割条圈地」之类的传说情节）在本页无法以可靠出处逐字核对，读者宜回查 [1][9] 原文。

## 2. 数学表述

### 2.1 Dido 问题（带直线边界的版本）

Dido 问题的标准陈述是：**求一条以给定直线为界的曲线，使它在给定周长下围出最大的面积**；其解是一条**半圆**（semicircle）[5]。换言之，直线本身充当了所求区域的「另一半边界」，故最优图形只是半个圆[5]。

来源 [6] 给出了等周长问题的另一种等价切入方式：求一条定长封闭曲线使其所围面积为最大；不失一般性，可假设曲线为凸函数，并可被 $x$ 轴平分，从而把闭曲线问题化为变分问题。这一「沿 $x$ 轴对称展开、把面积加倍而周长不变」的对称化归约，是连接「闭曲线版本」与「半平面版本」的关键步骤[6]。

### 2.2 等周定理与等周不等式

等周定理断言：在欧几里得平面上，周长相等的所有封闭图形中，**圆具有最大面积**；反之，面积相等的所有图形中，**圆的周长最小**[7][10]。定理的定量形式即**等周不等式**，它刻画了平面封闭图形的周长与面积之间的关系[8]。

用 $L$ 表示周长、$A$ 表示面积，则不等式为

$$L^2 \ge 4\pi A,$$

等号成立当且仅当图形为圆。两种表述的等价性如下表：

| 表述 | 给定 | 目标 | 最优图形 |
|---|---|---|---|
| 等周定理（表述 A） | 周长 $L$ | 面积 $A$ 最大 | 圆 |
| 等周定理（表述 B） | 面积 $A$ | 周长 $L$ 最小 | 圆 |
| Dido 问题 | 弧长 $L$ + 一条直线边界 | 面积最大 | 半圆 |

来源：[5][7][8][10]。

## 3. 变分法求解

### 3.1 泛函的建立

来源 [4][9] 指出，Dido 问题本质上是求曲线下方的面积最大化，需要变分法的工具；变分法的核心思想是寻找一个函数 $y(t)$，使得相应的积分泛函取极值[9]。以曲线 $y=y(x)$（$y(a)=y(b)=0$，端点在直线上）为例：

- 目标泛函（面积）：$A=\displaystyle\int_a^b y(x)\,\mathrm{d}x$；
- 约束泛函（弧长）：$K=\displaystyle\int_a^b \sqrt{1+y'(x)^2}\,\mathrm{d}x=L$。

### 3.2 Lagrange 乘子与 Euler–Lagrange 方程

等周问题是典型的**等周型约束变分问题**（isoperimetric problem in the calculus of variations）。标准处理方法是引入常数 $\lambda$，把带约束问题化归为求 $\int (L-\lambda K)\,\mathrm{d}x$ 的极值[11][12]；来源 [12] 特别说明，证明中必须用到 Lagrange 乘子，而常数 $\lambda$ 最终正是一个 Lagrange 乘子。自由度更多、约束更复杂的情形同样可用这一技术处理[13][14]。

对上节泛函取 $F=y-\lambda\sqrt{1+y'^2}$，Euler–Lagrange 方程为

$$1+\lambda\,\frac{y''}{(1+y'^2)^{3/2}}=0 .$$

其中 $\dfrac{y''}{(1+y'^2)^{3/2}}$ 正是曲线（带符号的）曲率 $\kappa$。因此极值曲线满足

$$\kappa=-\frac{1}{\lambda}=\text{常数},$$

即**曲率为常数的曲线**——圆（或其弧）。这与 [15] 所述一致：由标准变分方法加 Lagrange 乘子得到的 Euler–Lagrange 方程是非线性方程，其解给出几何形状。

### 3.3 结果

- 闭曲线情形：圆，半径 $R=L/(2\pi)$，最大面积 $A_{\max}=L^2/(4\pi)$，恰为等周不等式的等号情形。
- Dido 问题（一段弧 + 一条直线边界）：半圆，弧长 $L$ 对应半径 $R=L/\pi$，面积 $A=L^2/(2\pi)$，是同弧长下整圆面积的两倍——直观上因为直线边界"免费"提供了另外半个边界[5]。

## 4. 边界情形与经典变分法的局限

来源 [3]（Math StackExchange）专门讨论了「当长度超过半圆时」Dido 等周问题的解，并将其与**经典变分法的局限**联系起来。若把直线边界取为一条定长的直线段，则曲线两端点被固定，问题变为：给定弦长 $d$ 与弧长 $L$（$L\ge d$），求最大面积。此时极值曲线是以该线段为弦的圆弧；由 $L=2R\theta$、$d=2R\sin\theta$ 可得 $L(\theta)=d\theta/\sin\theta$（$\theta\in(0,\pi)$），该函数单调递增，故：

- 当 $L=\pi d/2$ 时，$\theta=\pi/2$，圆弧恰为半圆；
- 当 $L>\pi d/2$ 时，$\theta>\pi/2$，最优弧成为**优弧**，不再是 $y=y(x)$ 这类单值函数的图像。

这正是「长度超过半圆」处分岔的技术来源：单值函数参数化在此时失效，必须改用参数化曲线或分段处理。需要说明的是，上述推算由本页依据标准变分结果补出，**来源 [3] 仅以检索片段形式出现，其确切表述与所指的「局限」尚待核对**（见第 7 节）。

## 5. 严格化证明的历史（来源缺口）

来源 [10] 明确指出，等周定理的结论**早已为人所知，但其严格证明在历史上经历了很长过程**（该条目原文在这一点上被截断）。来源 [8] 亦将其定位为「几何中的不等式定理」。关于严格化的完整脉络（例如古代几何学家的初等论证、Euler 与 Lagrange 的分析方法、19 世纪由对称化与级数方法给出的严格证明等），本页所依据的检索材料**没有提供任何可核对的细节**，因此不作展开；相关文献建议见第 9 节。

## 6. 教学与常见理解要点

1. 等周问题是最基本的**等周问题族**的成员：这类问题的共同特征是「固定某种「周长型」量、优化「面积型」量」[2]。
2. 它同时是变分法的**入门样板**：Dido 问题要求最大化曲线下的面积，必须动用变分法工具[4]。
3. 它是**带约束极值**的标准示例：Lagrange 乘子在等周约束中不是可选项，而是证明的核心[12][11]。
4. 结论本身极为简洁（只用到一个约束条件「定长」），因此把「面积最大」理解为求极值、进而用变分法处理显得非常自然[9]。

## 7. 本 wiki 内部关联

本 wiki 现有条目主要来自《数学指南——实用数学手册》6.2–6.4 节的概率论与数理统计内容（如 [[随机过程]]、[[极限定理]]、[[数学指南-实用数学手册]]），与等周问题所属的**变分法与几何分析**方向暂无直接内容重叠。可作为弱关联的现有条目包括：

- [[魏尔斯特拉斯]] —— 分析学基础领域的代表人物条目；变分法的严格化与 Weierstrass 的工作密切相关（本关系为常识性关联，未由本页来源直接支持）。
- [[数学指南-实用数学手册]] —— 本 wiki 主要来源手册，可作为后续查证变分法章节是否收录等周问题的入口。

## 8. 矛盾、空白与待考问题

1. **来源 [3] 的「局限」含义未定**：来源以提问形式出现，未给出完整解答；本页第 4 节的解释是依据标准变分结果推得的，需以原文核对。
2. **严格化历史的空白**：来源 [8][10] 均指向「严格证明经历了长期过程」，但均未给出人名、年份或证明方法，本页无法补全。
3. **解的形式在两种版本间的差异**：闭曲线版本解为「圆」[7][10]，带直线边界版本解为「半圆」[5]。这并非矛盾，而是边界条件不同所致；但部分通俗材料未加区分，容易造成混淆。
4. **神话内容与数学内容混杂**：来源 [1][9] 将文学/神话叙事与数学问题并置，本页只能确认「名称与题材来自 Dido 传说」这一层，细节不可核实。
5. **证据质量整体偏弱**：本条目多数来源为百科条目、问答帖与通俗文章（[3][6][7][8][9][10]），仅 [1][4][6][12] 具有学术或教材性质，且多为片段。

## 9. 建议进一步检索的来源

- Blåsjö, V., *The Isoperimetric Problem*, The American Mathematical Monthly（公认的等周问题证明史综述，可填补第 5 节空白）。
- 英文维基百科 *Isoperimetric inequality* 条目（含古代几何证明、Euler、Schwarz 等历史线索）。
- Hilbert & Courant, *Methoden der mathematischen Physik* 的变分法章节（等周约束的经典处理）。
- Liberzon, *Calculus of Variations and Optimal Control Theory* 第 2 章（即来源 [4] 所在教材，含 Dido 问题的完整变分推导）。
- 來源 [6]《數學傳播》「等周長不等式」全文（凸性与 $x$ 轴平分归约的细节）。
- 来源 [1] 的 arXiv 全文（神话如何转化为数学问题的史学论述）。
- 关于 Steiner 对称化、Brunn–Minkowski 不等式与最优传输证明等**几何与测度论证明路线**的专门文献（本页来源完全未覆盖）。
- 关于等周不等式在非欧空间、图论与黎曼几何中的推广（如 Cheeger 常数）的入门综述。

## 参见

- [[数学指南-实用数学手册]]
- [[魏尔斯特拉斯]]
- [[随机过程]]、[[极限定理]]（本 wiki 现有分析/概率方向条目，仅作导航）

## References

1. [Dido's Problem: When a myth of ancient literature became a ... - arXiv](https://arxiv.org/html/2301.02917v1) — arxiv.org
2. [[PDF] This is probably the oldest problem in the Calculus of Variations. • Dido ...](https://www.liverpool.ac.uk/~maryrees/homepagemath302/m302_17_4_12article.pdf) — liverpool.ac.uk
3. [geometry - What is the solution to the Dido isoperimetric problem when ...](https://math.stackexchange.com/questions/2229845/what-is-the-solution-to-the-dido-isoperimetric-problem-when-the-length-is-longer) — math.stackexchange.com
4. [2.1.1 Dido's isoperimetric problem - Daniel Liberzon](http://liberzon.csl.illinois.edu/teaching/cvoc/node21.html) — liberzon.csl.illinois.edu
5. [Dido's Problem -- from Wolfram MathWorld](https://mathworld.wolfram.com/DidosProblem.html) — mathworld.wolfram.com
6. [數學傳播| 等周長不等式](https://www.math.sinica.edu.tw/mathmedia/journals/4543?keywords%5B%5D=%2A) — math.sinica.edu.tw
7. [谈谈变分法的基本应用（2） - 知乎专栏](https://zhuanlan.zhihu.com/p/496351029) — zhuanlan.zhihu.com
8. [等周定理- 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/%E7%AD%89%E5%91%A8%E5%AE%9A%E7%90%86) — zh.wikipedia.org
9. [等周定理：一个爱情悲剧里的数学问题 - 网易](https://www.163.com/dy/article/EUA81F2P0511C4OP.html) — 163.com
10. [等周不等式_百度百科](https://baike.baidu.com/item/%E7%AD%89%E5%91%A8%E4%B8%8D%E7%AD%89%E5%BC%8F/5392796) — baike.baidu.com
11. [Using Lagrange multiplier in Euler-Lagrange Equation](https://math.stackexchange.com/questions/3580992/using-lagrange-multiplier-in-euler-lagrange-equation) — math.stackexchange.com
12. [Isoperimetric Problems](https://www.homepages.ucl.ac.uk/~ucahmto/latex_html/chapter2_latex2html/node9.html) — homepages.ucl.ac.uk
13. [5.9: Lagrange multipliers for Holonomic Constraints](https://phys.libretexts.org/Bookshelves/Classical_Mechanics/Variational_Principles_in_Classical_Mechanics_(Cline)/05%3A_Calculus_of_Variations/5.09%3A_Lagrange_multipliers_for_Holonomic_Constraints) — phys.libretexts.org
14. [Euler-Lagrange Equation: Constraints and Multiple Dependent Variables](https://www.youtube.com/watch?v=pdO14dqC_nI) — youtube.com
15. [What to do when Euler Lagrange Equation is highly nonlinear ode?](https://mathoverflow.net/questions/326846/what-to-do-when-euler-lagrange-equation-is-highly-nonlinear-ode) — mathoverflow.net
