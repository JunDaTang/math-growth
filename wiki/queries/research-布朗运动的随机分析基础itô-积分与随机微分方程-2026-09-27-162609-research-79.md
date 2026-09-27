---
type: query
title: "Research: 布朗运动的随机分析基础（Itô 积分与随机微分方程）"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: 布朗运动的随机分析基础（Itô 积分与随机微分方程）

# 布朗运动的随机分析基础（Itô 积分与随机微分方程）

## 概述

随机分析（stochastic analysis，亦称 Itô 分析 / Itô calculus）以 [[布朗运动]]（即 [[维纳过程]]）为核心对象，把经典微积分的方法推广到 [[随机过程]] 之上 [1]。该理论以日本数学家 Kiyosi Itô 命名，其两大支柱是**对布朗运动的随机积分（Itô 积分）**与**随机微分方程（SDE, stochastic differential equation）**[1]。这一体系与本 wiki 已有的 [[费恩曼-卡茨公式]]、[[维纳积分]]、[[费恩曼积分]]、[[扩散方程]] 以及 [[科尔莫戈罗夫主定理]] 等内容处于同一知识脉络之中，可视为后者的现代随机分析版本。

---

## Itô 积分

### 与 Riemann–Stieltjes 积分的类比

Itô 积分可以按照与 Riemann–Stieltjes 积分类似的方式定义，即取 Riemann 和的**概率极限**；与经典情形不同的是，这样的极限未必逐轨道（pathwise）存在 [1]。设 $\{\pi_n\}$ 是一列区间 $[0,t]$ 的分割，其网格宽度趋于零，则 $H$ 关于 $B$ 直到时刻 $t$ 的 Itô 积分为随机变量

$$\int_0^t H\,dB = \lim_{n\to\infty}\sum_{[t_{i-1},t_i]\in\pi_n} H_{t_{i-1}}\,(B_{t_i}-B_{t_{i-1}})$$

其中被积函数在每段上取**左端点** $t_{i-1}$ 处的值 [1]。这一"提前取样"（predictable）的选择是 Itô 积分区别于 Stratonovich 积分的关键；若改取区间内部点（中点），则得到的是 Stratonovich 型积分。极限只在依概率收敛意义下存在，而非逐样本轨道收敛 [1]。

### 可积性与 Itô 等距

若 $H$ 是任一 predictable 过程，且对每个 $t\ge 0$ 有 $\int_0^t H^2\,ds<\infty$，则 $H$ 关于 $B$ 的积分可以定义，此时称 $H$ 是 *$B$-可积*（$B$-integrable）的 [1]。此时该积分同样以依概率收敛的极限给出 [1]。

Itô 积分满足 **Itô 等距**（Itô isometry）：

$$\mathbb{E}\!\left[\left(\int_0^t H_s\,dB_s\right)^2\right]=\mathbb{E}\!\left[\int_0^t H_s^2\,ds\right]$$

对简单的 predictable 被积函数，该等距可由布朗运动增量相互独立、均值为零且 $\mathrm{Var}(B_t)=t$ 这一性质加以证明；随后借助连续线性延拓，把定义唯一地延拓到所有满足 $\mathbb{E}[H^2\cdot\langle M\rangle_t]<\infty$ 的 predictable 被积函数上 [1]。

### 构造策略

Itô 积分的标准构造遵循"先简单、后逼近"的两步思路 [3]：

1. 先对一类**简单函数** $\varphi$ 定义积分 $I[\varphi]$；
2. 再证明每个 $f\in V$ 都可以在适当意义下由这类 $\varphi$ 逼近。

这一"简单过程—等距—完备化—延拓"的框架，是实分析与测度论中先对有限可测简单函数定义积分再作延拓的思路在随机情形的对应物。

---

## Itô 过程

**Itô 过程**定义为一个适应的（adapted）随机过程，它可以表示为"关于布朗运动的积分"与"关于时间的积分"之和 [1]：

$$X_t = X_0 + \int_0^t \mu_s\,ds + \int_0^t \sigma_s\,dB_s$$

其中 $B$ 是布朗运动，要求 $\sigma$ 是 predictable 且 $B$-可积的过程，$\mu$ 是 predictable 且（[[维纳|Lebesgue]] 意义下）可积的过程 [1]。这一形式是 SDE 的积分形式，其微分写法即为

$$dX_t = \mu_t\,dt + \sigma_t\,dB_t.$$

值得注意的是，Itô 积分最初的经济学解释正是"连续时间交易策略的收益"：以 $H_t$ 表示时刻 $t$ 持有股票的数量，则 $\int H\,dB$ 对应一笔连续交易策略的收益 [1]。

---

## Itô 公式与随机微分方程

Itô 分析中用于"换元"的工具是 **Itô 公式**（Itô's lemma）。其典型用法可通过几何布朗运动（geometric Brownian motion）说明：给定 SDE

$$dX(t) = X(t)\bigl(\mu\,dt + \sigma\,dW(t)\bigr),$$

对函数 $f(X(t))=\log X(t)$ 应用 Itô 公式，即可解出该 SDE [2]。这说明 Itô 公式在结构上类似于链式法则，但由于布朗运动轨道具有非零二次变差，换元时会多出二阶修正项。

> **来源说明**：来源 [2] 仅以示例方式提及 Itô 公式的用法，来源 [1] 的摘要亦未展开 Itô 公式的完整陈述。因此本页不对 Itô 公式的具体形式（如 $d f = f'(X)dX + \tfrac12 f''(X)\,d\langle X\rangle$）作超出源材料的断言，详见下文"空白与待补充"。

---

## 费恩曼-卡茨公式：SDE 与偏微分方程的桥梁

**费恩曼-卡茨公式**（Feynman–Kac formula）由 [[费恩曼|Richard Feynman]] 与 [[卡茨|Mark Kac]] 命名，在抛物型偏微分方程与随机过程之间建立联系 [7]。它一方面给出用随机轨道模拟求解某类 PDE 的方法，另一方面也可用确定性的方式计算随机过程的一类重要期望 [7]。

### 一个显式算例

对某类可解析求解的 PDE，其解可写成条件期望形式 [7]：

$$u(x,t)=\mathbb{E}\!\left[e^{-X_T^2}\,\bigl|\,X_t=x\right],\qquad dX_t = dt+\sqrt{2}\,dW_t,$$

其中 $X$ 是由上述 SDE 驱动的 Itô 过程，$W_t$ 是 [[维纳过程|Wiener 过程]]；而同一 $u(x,t)$ 又有解析表达式

$$u(x,t)=\frac{1}{\sqrt{5-4t}}\exp\!\left(-\frac{(1-t+x)^2}{5-4t}\right).$$

这说明在确定性 PDE 求解器难以处理的情形（如高维或内含不确定性）下，随机微分方程提供了一种灵活且可扩展的替代途径，而 Euler–Maruyama 等数值方法可用于逼近 PDE 的解 [7]。

### 金融解释

在金融中，若以 $(X_T-K)^+$ 表示看涨期权到期收益，则期权在时刻 $t$、股价 $x$ 处的风险中性价格为 [7]

$$u(x,t)=\mathbb{E}\!\left[e^{-\int_t^T r_s\,ds}(S_T-K)^+\;\Big|\;\ln S_t=\ln x\right],$$

即费恩曼-卡茨公式之下的一类贴现期望。

### 与已有概念的呼应

本 wiki 已有的 [[费恩曼-卡茨公式]]、[[费恩曼积分]]、[[虚时间布朗运动]] 条目，均通过实时间/虚时间的对比把 [[扩散方程]] 与 [[薛定谔|薛定谔方程]] 联系起来；来源 [6] 亦指出费恩曼-卡茨公式正是薛定谔方程在时间被复化（complexified）时的费恩曼积分表示，可视为对既有叙述的补充证据。来源 [10] 进一步说明，该公式对扩散过程给出二阶偏微分方程解的随机表示，并可推广到 switching diffusions 等更一般情形。

---

## 布朗运动的存在性与构造

Itô 积分理论的出发点——布朗运动的存在性——通常借助 Kolmogorov 扩张定理建立 [11][12][14][15]。其标准路线为：先指定所需的有限维分布（有限维边缘分布的相容族），再用 Kolmogorov 扩张定理得到函数空间 $\mathbb{R}^T$ 上的概率测度 $P$，从而在某个概率空间 $(\Omega,\mathcal{F},P)$ 上支持一个布朗运动 [15]。该测度即本 wiki 已收录的 [[维纳测度]]，它是历史上第一个定义在函数空间上的概率测度 [13]。相关的历史与理论脉络可参见 [[科尔莫戈罗夫主定理]]、[[柱面集]]、[[随机过程的联合分布函数族]] 与 [[随机过程的实现]]。

> **形式化进展**：来源 [13] 报告了在 Lean 证明助手中对布朗运动的形式化工作，指出布朗运动引出了 Wiener 测度这一函数空间上的首个概率测度，属于把随机分析严格化并机器验证的当代努力。

---

## 与既有 wiki 内容的衔接

| 本页主题 | 关联的已有条目 |
|---|---|
| Itô 积分的被积过程 | [[随机过程]]、[[布朗运动]] |
| 积分的概率测度基础 | [[维纳测度]]、[[柱面集]] |
| 积分的期望性质 | [[布朗运动的转移概率]]、[[布朗运动转移密度]] |
| SDE 与 PDE 的对偶 | [[费恩曼-卡茨公式]]、[[扩散方程]]、[[费恩曼积分]] |
| 存在性基础 | [[科尔莫戈罗夫主定理]]、[[科尔莫戈罗夫]] |
| 历史人物 | [[维纳]]、[[费恩曼]]、[[卡茨]] |

凡涉及布朗运动轨道性质、转移概率与扩散方程的既有结论，均可由本页的 [[wikilink]] 直接追溯到 [[64412节布朗运动转移概率格子随机游走与扩散方程]] 与 [[6443节维纳测度构造与维纳过程性质]] 等来源笔记。

---

## 矛盾、局限与空白

1. **Itô 公式的完整表述缺失**：来源 [1] 的摘要只给出积分、Itô 等距与 Itô 过程的定义，没有给出 Itô 公式的一般陈述；来源 [2] 仅以几何布朗运动为例提示用法。因此本页无法据现有材料给出 Itô 公式的严格形式，需补充教材级来源。
2. **Stratonovich 积分仅被隐含对照**：来源 [1] 指出极限"不逐轨道存在"以及取左端点的约定，但未系统比较 Itô 与 Stratonovich 积分。二者关系（Itô–Stratonovich 修正项）在本页中仍属空白。
3. **鞅性与半鞅框架只被提及**：来源 [1] 提到被积过程可推广到 semimartingale，但未展开鞅表示定理、二次变差 $\langle M\rangle_t$ 的定义等基础概念，而 Itô 等距的延拓条件恰依赖 $\langle M\rangle_t$ [1]。
4. **一维假设**：来源 [5] 明确只定义实值过程关于**一维**布朗运动的随机积分，并声明可作推广但未展开；来源 [4] 则在向量格（vector lattice）中构造 Itô 积分，属于更抽象的方向。多维与抽象值情形的细节在本页中未覆盖。
5. **来源质量参差**：来源 [2]、[9] 来自问答/论坛类平台，权威性较低；[11]、[12] 同属 Math StackExchange / MathOverflow 社区，宜与 [14]、[15] 的讲义材料交叉验证。

---

## 建议补充的来源

- **标准教材**：Øksendal《Stochastic Differential Equations》、Karatzas & Shreve《Brownian Motion and Stochastic Calculus》、Revuz & Yor《Continuous Martingales and Brownian Motion》（来源 [1] 引用的正是 Revuz–Yor 第 IV 章）。这些可补齐 Itô 公式、二次变差、鞅表示与多维积分的严格陈述。
- **Itô 公式与 Itô–Stratonovich 关系的独立条目**：用于把本页的空白 (1)(2) 补全。
- **Girsanov 定理与测度变换**：与金融定价中的风险中性测度直接相关，可补来源 [7] 金融应用背后的理论基础。
- **Euler–Maruyama 数值方法**：来源 [7]、[8] 提到该方法用于由 SDE 逼近 PDE 解，但目前来源 [8] 仅给出流程提纲（"定义模型参数 → 应用 Itô 法则 → 求解 Feynman–Kac 方程"）[8]，需要更细致的数值分析来源。
- **Kolmogorov 扩张定理的严格陈述**：用以支撑"布朗运动存在性"一节，使本页与 [[科尔莫戈罗夫主定理]] 的连接更完整。
- **形式化验证文献**：来源 [13] 的 Lean 形式化工作可作为"随机分析严格化"的当代入口，值得进一步查阅。

---

## 相关条目

[[布朗运动]]、[[维纳过程]]、[[维纳测度]]、[[维纳积分]]、[[费恩曼-卡茨公式]]、[[费恩曼积分]]、[[扩散方程]]、[[虚时间布朗运动]]、[[随机过程]]、[[科尔莫戈罗夫主定理]]、[[维纳]]、[[费恩曼]]、[[卡茨]]、[[科尔莫戈罗夫]]、[[数学指南-实用数学手册]]

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
11. [Existence of Brownian motion using Kolmogorov's extension theorem](https://mathoverflow.net/questions/455616/existence-of-brownian-motion-using-kolmogorovs-extension-theorem) — mathoverflow.net
12. [Definition/Construction of Wiener Measure - Math Stack Exchange](https://math.stackexchange.com/questions/1725487/definition-construction-of-wiener-measure) — math.stackexchange.com
13. [Formalization of Brownian motion in Lean - arXiv](https://arxiv.org/html/2511.20118v1) — arxiv.org
14. [[PDF] STOCHASTIC PROCESSES AND CONSTRUCTION OF BROWNIAN ...](https://infoscience.epfl.ch/bitstreams/d0548bf7-1549-48dc-beaf-be76c1008270/download) — infoscience.epfl.ch
15. [[PDF] ) = 7N(0, 1) D](https://www.math.ucla.edu/~biskup/275d.1.25f/PDFs/ch4.pdf) — math.ucla.edu

## Related
- [[queries/research-布朗运动的随机分析基础itô-积分与随机微分方程-2026-09-27-162817-research-80]]
