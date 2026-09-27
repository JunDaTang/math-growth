---
type: query
title: "Research: 布朗运动的随机分析基础：Itô 积分与随机微分方程"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: 布朗运动的随机分析基础：Itô 积分与随机微分方程

# 布朗运动的随机分析基础：Itô 积分与随机微分方程

## 概述

**Itô 分析**（Itô calculus）以数学家 Kiyosi Itô（伊藤清）命名，其目标是把经典微积分的方法推广到 [[布朗运动]]（即 [[维纳过程]]）这类 [[随机过程]] 上 [1]。整套理论的核心构件包括：Itô 积分、Itô 等距、Itô 过程（随机微分方程）以及 Itô 公式，它们共同构成对布朗运动做“随机微积分”运算的基础 [1]。

从应用角度看，Itô 随机积分可以被解释为一种连续时间交易策略的收益：在时刻 $t$ 持有数量 $H_t$ 的股票，其累计收益即 $\int_0^t H\,dB$ [1]。这一金融解释使 Itô 积分成为数理金融（如期权定价）的语言基础 [1][7]。

本页综合若干来源，梳理该理论的三条主线：**Itô 积分的构造**、**Itô 过程与随机微分方程**、以及与之紧密关联的**费恩曼-卡茨公式**；最后回到**维纳测度与布朗运动的存在性基础**，与本站既有的 [[数学指南-实用数学手册]] 系列条目衔接。

---

## Itô 积分的构造

### 与 Riemann–Stieltjes 积分的类比及差异

Itô 积分可以按照与 [[维纳积分|Riemann–Stieltjes 积分]] 类似的方式定义，即取**依概率收敛**的 Riemann 和之极限 [1]。此处与经典积分有一个关键区别：**这一极限未必逐路径（pathwise）存在** [1]。也就是说，Itô 积分本质上是一个随机变量，而非对每条样本轨道分别定义的逐点极限。

### 依概率极限的定义式

设 $\{\pi_n\}$ 是一列 $[0,t]$ 的分割，其网格宽度趋于零，则 $H$ 关于布朗运动 $B$ 到时刻 $t$ 的 Itô 积分定义为随机变量 [1]：

$$\int_0^t H\,dB = \lim_{n\to\infty}\sum_{[t_{i-1},t_i]\in\pi_n} H_{t_{i-1}}\,(B_{t_i}-B_{t_{i-1}}).$$

注意被积函数取值于每个子区间的**左端点** $t_{i-1}$，这一“左端点约定”正是 Itô 积分区别于 Stratonovich 积分的标志性特征（本条未在来源中展开）。

### 构造的三步方案

构造遵循一种标准的分层策略 [3]：

1. 先对**一类简单的函数 $\varphi$** 定义积分 $I[\varphi]$；
2. 证明任意 $f\in V$ 都可在适当意义下由这类 $\varphi$ 逼近；
3. 由此把积分延拓到更一般的被积过程。

被积过程的适用范围是：只要 $H$ 是任何**可料过程**（predictable process）且满足对每个 $t\ge0$ 都有 $\int_0^t H^2\,ds<\infty$，则 $H$ 关于 $B$ 的积分即可定义，此时称 $H$ 是 **$B$-可积的** [1]。更一般地，被积过程 $H$ 可取为关于 $X$ 生成的 [[柱面集|σ-代数流]] 局部平方可积且适应的过程，其中 $X$ 是布朗运动，或更一般地是一个**半鞅**（semimartingale）[1]。

### Itô 等距

构造得以成立的关键恒等式是 **Itô 等距**（Itô isometry）[1]：

$$\mathbb{E}\!\left[\left(\int_0^t H_s\,dB_s\right)^2\right] = \mathbb{E}\!\left[\int_0^t H_s^2\,ds\right].$$

对简单可料被积函数，该等距可由布朗运动“**独立增量、零均值、方差 $\mathrm{Var}(B_t)=t$**”这三条性质直接证明 [1]。随后通过**连续线性延拓**，可唯一地把积分延拓到所有满足 $\mathbb{E}[H^2\cdot\langle M\rangle_t]<\infty$ 的可料被积过程上 [1]。

---

## Itô 过程与随机微分方程

**Itô 过程**（Itô process）定义为可表示为“关于布朗运动的积分”与“关于时间的积分”之和的适应随机过程 [1]：

$$X_t = X_0 + \int_0^t \mu_s\,ds + \int_0^t \sigma_s\,dB_s,$$

其中 $B$ 为布朗运动，要求 $\sigma$ 是可料且 $B$-可积的过程，$\mu$ 是可料且（Lebesgue）可积的过程 [1]。写成微分形式即通称的**随机微分方程**（SDE）：

$$dX_t = \mu_t\,dt + \sigma_t\,dB_t.$$

来源中给出的典型例子包括：

- **几何布朗运动**：$dX(t)=X(t)\bigl(\mu\,dt+\sigma\,dW(t)\bigr)$，其求解通常借助 Itô 公式，取 $f(X(t))=\log X(t)$ [2]；
- **带漂移的常系数扩散**：$dX_t = dt+\sqrt2\,dW_t$，其中 $W_t$ 为 [[维纳过程]] [7]。

这些例子提示：SDE 的求解往往归结为对某个函数 $f$ 应用 Itô 公式（即“伊藤引理”），从而把关于 $X$ 的积分转化为关于 $B$ 和 $t$ 的显式表达式 [2]。

---

## 费恩曼-卡茨公式

### 公式的意义

[[费恩曼-卡茨公式]]以 [[费恩曼|Richard Feynman]] 与 [[卡茨|Mark Kac]] 命名，它在**抛物型偏微分方程**与 [[随机过程]] 之间建立了桥梁 [7]。该公式有两重用途 [7]：

- 通过模拟随机路径来求解某些偏微分方程；
- 反过来，把某一类重要的随机过程期望值用确定性方法（解 PDE）计算出来。

这正是本站既有条目 [[64445节费恩曼卡茨公式与费恩曼积分]] 中，从布朗运动与薛定谔方程形式对应角度所讨论同一公式的另一视角。这里强调其在**二阶抛物型 PDE** 语境下的“期望表示”作用；来源也指出，对一般扩散过程，费恩曼-卡茨公式为某些二阶偏微分方程的解提供随机表示 [10]。

### 一个显式例子

对某个初值问题，方程可解析求解为 [7]

$$u(x,t)=\frac{1}{\sqrt{5-4t}}\exp\!\left(-\frac{(1-t+x)^2}{5-4t}\right),$$

而应用费恩曼-卡茨公式，其解又可写成条件期望 [7]：

$$u(x,t)=\mathbb{E}\!\left[e^{-X_T^2}\,\bigl|\,X_t=x\right],$$

其中 $X$ 是由 SDE $dX_t=dt+\sqrt2\,dW_t$ 驱动的 Itô 过程。该例说明：**随机模拟（配合 Euler–Maruyama 等数值方法）可以近似 PDE 的解** [7]。因此，在不确定性内蕴或维数构成计算障碍的场合，随机微分方程提供了相对确定性 PDE 求解器更灵活、更可扩展的替代方案 [7]。

### 数值工作流与应用

MathWorks 给出的实现思路概括为三步 [8]：

1. 用随机微分方程定义模型参数；
2. 应用 Itô 法则（Itô 公式）；
3. 求解费恩曼-卡茨方程。

在应用侧，金融是典型场景：设期权到期收益为 $(X_T-K)^+$，则期权在时刻 $t$、股价 $x$ 处的风险中性价格为 [7]

$$u(x,t)=\mathbb{E}\!\left[e^{-\int_t^T r_s\,ds}(S_T-K)^+\;\Bigl|\;\ln S_t=\ln x\right].$$

此外，费恩曼-卡茨公式还被推广到**切换扩散**（switching diffusions）等更一般的框架，用以刻画连续时间马尔可夫切换模型的期望表示 [10]。

---

## 维纳测度与布朗运动的存在性基础

Itô 积分与 SDE 的严格化离不开“布朗运动作为一个概率空间上的随机过程”的构造。这条线索由科尔莫戈罗夫型延拓定理承担：

- **Kolmogorov 延拓定理**为“给定一族有限维分布、即可构造相容的测度”给出条件，其推论涵盖 [[维纳过程]] 以及马尔可夫过程等对象 [13]。借助该定理，可以在 $\mathbb{R}^{\mathbb{Q}\cap[0,\infty)}$ 或 $\mathbb{R}^{[0,T]}$ 这类乘积空间上构造测度 $\mu$，再把**维纳测度** $\nu$ 定义在 $C[0,\infty)$ 上 [11][12]。
- **Daniell–Kolmogorov 延拓定理**被列为随机过程理论中最早、最深刻的定理之一 [15]。
- 在应用层面，先构造有限的投影测度、再套用延拓定理，是构造布朗运动的标准路径；具体实现时需要“先显式构造 $\mathbb{R}^k$ 上的概率测度，再套用延拓定理” [14]。

这一构造链条与本站已有条目直接衔接：[[科尔莫戈罗夫主定理]]及其 [[645节随机过程一般定义与科尔莫戈罗夫主定理]]，以及 [[维纳测度]] 的构造（见 [[6443节维纳测度构造与维纳过程性质]]）正是此处“存在性基础”的详细来源。Itô 积分则可视为在这些过程之上进一步施加“随机微积分”运算的层级。

---

## 与既有 wiki 内容的联系

- **布朗运动/维纳过程**：[[布朗运动]]、[[维纳过程]] 提供了被积分对象（积分器）的轨道与概率性质；Itô 积分正是在其独立性、零均值、方差线性等性质之上构造的 [1]。
- **布朗运动的转移结构**：[[布朗运动的转移概率]]、[[布朗运动转移密度]] 与 [[扩散方程]] 是费恩曼-卡茨公式右侧的条件期望所依赖的底层对象 [7]。
- **费恩曼积分与费恩曼-卡茨公式**：[[费恩曼积分]]、[[64445节费恩曼卡茨公式与费恩曼积分]] 与本站 [[费恩曼-卡茨公式]] 条目互为补充；本页补充了抛物型 PDE 语境下的“期望表示”这一侧面 [7][10]。
- **维纳测度的构造**：[[维纳测度]]、[[柱面集]]、[[科尔莫戈罗夫主定理]]、[[科尔莫戈罗夫]] 与 [[维纳]] 构成存在性基础链条 [11][12][13][15]。

---

## 矛盾、空白与待澄清之处

1. **定义式在来源中被截断**：[1] 的关键公式（一般 Itô 积分定义、Itô 等距、Itô 过程定义式）在抓取文本中以图片或空占位符出现，正文公式缺失，导致“一般半鞅情形的定义”与“关于布朗运动的定义”之间的过渡表述不够完整。建议核对原始条目以补全公式。
2. **逐路径极限不存在与“可料”条件的因果**：来源强调 Riemann 和的极限“未必逐路径存在”且为依概率收敛 [1]，但未说明被积函数为何必须取**可料**（而非仅适应）过程；这一细节（可料性保证积分作为鞅的性质）在来源中缺失。
3. **Itô 公式/引理本身未系统给出**：多个来源都提到“应用 Itô 公式” [2][8]，但均未给出引理的一般陈述（即 $df(X_t)$ 的展开式）。这是本页最主要的空白。
4. **Stratonovich 对照缺失**：由“左端点约定”所隐含的 Stratonovich 积分对照在全部来源中均未出现。
5. **费恩曼-卡茨公式的假设条件不明**：[7][10] 给出了公式的思想与算例，但未列出使该表示成立的边界条件、增长条件或椭圆/抛物型算子前提。
6. **两处“费恩曼-卡茨/费恩曼积分”表述需协调**：本站既有条目侧重“薛定谔方程的形式对应与费恩曼积分”，本页来源侧重“抛物型 PDE 的期望表示” [7]。二者是同一族定理的不同侧面，但若不加说明，易被误读为两种不同公式。

---

## 建议补充的来源

- **Itô 公式/引理的标准陈述**：如 Oksendal《Stochastic Differential Equations》或 Revuz–Yor 的专章，用以补足本页第 3 条空白。
- **Stratonovich 积分**：用于对照 Itô 与 Stratonovich 两种约定的差异及其在物理建模中的取舍。
- **鞅论与半鞅积分**：来源 [1] 已提及半鞅与 $\langle M\rangle_t$，但缺少对 Doob–Meyer 分解、可选二次变差的系统引证。
- **向量格框架下的 Itô 积分**：[4] 展示了在向量格（vector lattice）中构造布朗运动 Itô 积分的推广，可作为测度论推广方向的补充。
- **数值方法**：Euler–Maruyama 及 Milstein 格式的系统介绍，用于支撑 [7][8] 提到的随机模拟求解 PDE 的主张。
- **Daniell–Kolmogorov 定理的严格陈述**：[15] 提供了入口，建议进一步查找其测度论证明与其与 [[科尔莫戈罗夫主定理]] 的关系。
- **切换扩散中的费恩曼-卡茨**：[10] 仅为综述性入口，建议补足切换扩散的漂移/扩散项与生成算子定义。

---

## 参考来源

[1] Itô calculus — Wikipedia（en.wikipedia.org）
[2] How to solve the simple Ito (stochastic) integral over Brownian motion — math.stackexchange.com
[3] The construction of the Itô integral — Uni Ulm（PDF）
[4] The Itô integral for Brownian motion in vector lattices: Part 1 — ScienceDirect
[5] Brownian motion and Itô calculus — WIAS Berlin（PDF）
[6] Feynman-Kac formula for general time dependent stochastic parabolic … — arXiv
[7] Feynman–Kac formula — Wikipedia
[8] Simulate a Stochastic Process Using the Feynman-Kac Formula — mathworks.com
[9] Feynman Kac theorems for ODE — reddit.com
[10] Feynman-Kac formula for switching diffusions — link.springer.com
[11] Definition/Construction of Wiener Measure — math.stackexchange.com
[12] Wiener measure — USC Dornsife（PDF）
[13] Kolmogorov extension theorem — Wikipedia
[14] Existence of Brownian motion using Kolmogorov's extension theorem — mathoverflow.net
[15] Lecture 5. The Daniell-Kolmogorov existence theorem — fabricebaudoin.blog

## References

1. [Itô calculus - Wikipedia](https://en.wikipedia.org/wiki/It%C3%B4_calculus) — en.wikipedia.org
2. [How to solve the simple Ito (stochastic) integral over Brownian ...](https://math.stackexchange.com/questions/4401942/how-to-solve-the-simple-ito-stochastic-integral-over-brownian-motion-via-the-i) — math.stackexchange.com
3. [[PDF] The construction of the Itô integral. - Uni Ulm](https://www.uni-ulm.de/fileadmin/website_uni_ulm/mawi.inst.110/lehre/ss15/Seminar/Ito_Integral.pdf) — uni-ulm.de
4. [The Itô integral for Brownian motion in vector lattices: Part 1 - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0022247X14007525) — sciencedirect.com
5. [[PDF] brownian motion and itˆo calculus](https://www.wias-berlin.de/people/bayerc/files/shortcourse.pdf) — wias-berlin.de
6. [Feynman-Kac formula for general time dependent stochastic parabolic ...](https://arxiv.org/html/2508.07793) — arxiv.org
7. [Feynman–Kac formula - Wikipedia](https://en.wikipedia.org/wiki/Feynman%E2%80%93Kac_formula) — en.wikipedia.org
8. [Simulate a Stochastic Process Using the Feynman-Kac Formula](https://www.mathworks.com/help/symbolic/simulate-a-stochastic-process-by-feynman-kac-formula.html) — mathworks.com
9. [Feynman Kac theorems for ODE - a connection between stochastic ...](https://www.reddit.com/r/math/comments/oqj0we/feynman_kac_theorems_for_ode_a_connection_between/) — reddit.com
10. [Feynman-Kac formula for switching diffusions: connections of systems ...](https://link.springer.com/article/10.1186/1687-1847-2013-315) — link.springer.com
11. [Definition/Construction of Wiener Measure - Math Stack Exchange](https://math.stackexchange.com/questions/1725487/definition-construction-of-wiener-measure) — math.stackexchange.com
12. [[PDF] Wiener measure - USC Dornsife](https://dornsife.usc.edu/sergey-lototsky/wp-content/uploads/sites/211/2023/06/Week8-ByDiogo.pdf) — dornsife.usc.edu
13. [Kolmogorov extension theorem - Wikipedia](https://en.wikipedia.org/wiki/Kolmogorov_extension_theorem) — en.wikipedia.org
14. [Existence of Brownian motion using Kolmogorov's extension theorem](https://mathoverflow.net/questions/455616/existence-of-brownian-motion-using-kolmogorovs-extension-theorem) — mathoverflow.net
15. [Lecture 5. The Daniell-Kolmogorov existence theorem](https://fabricebaudoin.blog/2012/03/25/lecture-5-the-daniell-kolmogorov-existence-theorem/) — fabricebaudoin.blog

## Related
- [[queries/research-布朗运动的随机分析基础itô-积分与随机微分方程-2026-09-27-162609-research-79]]
