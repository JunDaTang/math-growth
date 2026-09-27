---
type: query
title: "Research: 高斯（Carl Friedrich Gauss）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 高斯（Carl Friedrich Gauss）

# 高斯（Carl Friedrich Gauss）

## 概述

卡尔·弗里德里希·高斯（Carl Friedrich Gauss, 1777—1855）是德国数学家，在数理统计史上最常被提及的贡献集中在两条线索上：**最小二乘法**（method of least squares）与**误差的正态分布理论**。后世把正态分布称为「高斯分布」，正是因为高斯在 1809 年的《Theoria motus corporum coelestium》（天体运动理论）中把误差的概率分布引入观测数据的处理，使误差分析第一次具有了概率论基础 [1][14]。这一工作与 [[正态分布]]、[[高斯钟形曲线]] 以及 [[概率密度]] 等既有条目直接相关：高斯并没有「发明」钟形曲线本身，但他是把这条曲线确立为测量误差的默认模型的关键人物 [13]。

## 关键事件年表

| 时间 | 事件 | 来源 |
| --- | --- | --- |
| 1801-01-01 | Piazzi 发现谷神星（Ceres），持续观测后被太阳光辉淹没 | [9] |
| 1801 | 24 岁的高斯用最小二乘分析预测谷神星重现位置，唯一成功 | [7][9] |
| 1801-12-31 | Olbers 在高斯预言的时间与位置找到谷神星 | [2] |
| 1805 | Legendre 首次公开发表最小二乘法 | [6][9] |
| 1808 | 美国的 Robert Adrain 独立提出类似想法 | [11] |
| 1809 | 高斯发表《Theoria motus》，给出最大似然、最小二乘与正态分布 | [11][14] |
| 1810 | Laplace 读高斯著作后，用中心极限定理给出大样本辩护 | [9] |
| 1823 | 高斯发表《Theoria combinationis observationum erroribus minimis obnoxiae》 | [6] |

## 谷神星事件与方法保密

谷神星问题的困难在于：天文学家希望在它从太阳背后重新出现后确定其位置，又不想去解 Kepler 那套复杂的非线性行星运动方程 [9]。高斯以其数学才能创立了一种崭新的行星轨道计算方法，据报道「一个小时之内」就算出了轨道并预言了它出现的时间与位置 [2]。1801 年 12 月 31 日夜，德国天文爱好者奥伯斯（Heinrich Olbers）在高斯预言的时间对准天空，谷神星果然出现 [2]。也有叙述强调，在尝试高斯预测之后的第一个晴夜，谷神星就出现在他所说的位置上 [7]。

高斯当时拒绝透露计算轨道的方法，原因可能是他认为方法的理论基础还不够成熟；他一向治学严谨，不轻易发表没有思考成熟的理论 [2]。直到 1809 年他系统完善相关数学理论后，才把方法公布于众，其中使用的数据分析方法就是以正态误差分布为基础的最小二乘法 [2]。

> **细节分歧**：谷神星被跟踪的时长，[9] 记为 40 天，[2] 记为「在夜空中出现 6 个星期，扫过八度角」。两说大体一致但不完全等同，属叙述性差异。

## 最小二乘法与发明权之争

高斯在《Theoria motus》（1809）中声称自己自 1794 或 1795 年起就已使用最小二乘法，而该方法最早由 Adrien-Marie Legendre 在 1805 年发表；在统计学史上，这一分歧被称为「最小二乘法发明权之争」（priority dispute over the discovery of the method of least squares）[6][9]。值得注意的是，[2] 直接把这场争端与牛顿—莱布尼茨的微积分发明权之争相提并论，称其为数学史上仅次于后者的争端。

不过，多方来源一致认为高斯「超越了 Legendre」：他把最小二乘法与概率原理、正态分布联系起来，完成了 Laplace 关于「为观测指定一个依赖有限个未知参数的概率密度形式」的纲领 [9]。因此争论的焦点是**谁先发表**，而非**谁的贡献更大** [6][9]。

现代语境下，最小二乘法的表述通常涉及 [[测量序列]] 与 [[经验均值]] 等概念：它要求使误差平方和取最小。

## 高斯如何导出正态分布

### 1809 年的极大似然路线

[2] 给出了一条清晰的推导脉络：设真值为 θ，x₁,…,xₙ 为 n 次独立测量值，每次测量的误差为 eᵢ = xᵢ − θ，误差的密度函数为 f(e)。高斯要求「误差分布导出的极大似然估计 = 算术平均值」，即在所有概率密度函数中寻找唯一的 f，使得极大似然估计恰好是算术平均。高斯证明，满足这一性质的唯一概率密度就是

$$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{x^2}{2\sigma^2}}$$

即 [[正态分布]] 密度 [2]。在 [14] 的表述中，这一结论被概括为：**如果测量误差服从正态分布，那么算术平均就是真值的最可能取值**——高斯在 1809 年的《Theoria motus》中展示了这一点。

### 对最小二乘法的解释

进一步，高斯基于该误差分布对最小二乘法给出了很漂亮的解释：对于最小二乘公式中涉及的每个误差 eᵢ，若误差服从 N(0, σ²)，则 (e₁,…,eₙ) 的联合概率为

$$\frac{1}{(\sqrt{2\pi}\sigma)^n}\exp\left\{-\frac{1}{2\sigma^2} \sum_{i=1}^n e_i^2 \right\}$$

要使这个概率最大，必须使 Σeᵢ² 取最小值，这正好就是最小二乘法的要求 [2]。换句话说，**最小二乘法就是误差满足正态分布假设下的极大似然估计**；最小化平方误差本质上等同于误差服从高斯分布假设下的最大似然估计 [4]。

### 后世的使用惯性

[1] 指出，正态分布并非高斯最先发现，但由于高斯对误差项的研究，引起了人们对正态分布的重视，因此正态分布又叫高斯分布；现在人们一碰到有误差存在的情形，几乎总是假设误差服从均值为 0、方差为 σ 的正态分布，正是源自高斯，现代误差理论也从这里开始起步 [1]。机器学习中的常见做法——假定样本误差独立、可令均值归零（因为有截距 b）、服从均值为 0、方差为定值的正态分布——同样被追溯到这一传统 [3]。

## 1823 年《Theoria combinationis》与 Gauss–Markov 定理

据 [8]，高斯处理误差的意义远超最小二乘法本身：他把误差当作随机变量来处理，这本身就是对数学统计学的重要贡献。他在这一工作中引入的新概念包括：

1. 把误差视为随机变量；
2. 一个类 Chebyshev 的不等式；
3. 样本均值与方差的收敛性。

在两部分论文《Theoria combinationis observationum erroribus minimis obnoxiae》（1823）中 [6]：

- 第一部分证明了对单峰分布的 **Gauss 不等式**（Gauss's inequality，一类 Chebyshev 型不等式），并在未加证明的情况下陈述了关于四阶矩的另一个不等式（**Gauss–Winckler 不等式**的特例）；他还推导了样本方差的上下界。
- 第二部分描述了**递归最小二乘法**（recursive least squares），并称这是高斯发现的。
- 在误差均值为零、互不相关、正态分布且方差相等的线性模型下，最小二乘估计是系数的最佳线性无偏估计（best linear unbiased estimator），该结果的扩展版本即 **Gauss–Markov 定理** [6][9]。

高斯的误差理论后来被大地测量学家 Friedrich Robert Helmert 沿多个方向扩展为 **Gauss–Helmert 模型** [6]。

## 「循环论证」争议

高斯 1809 年的推导受到的最主要批评是**循环论证**。Stigler 指责高斯在处理最小二乘法时是循环的：他先假设误差的正态性，据此导出方法，然后又用「该方法被普遍使用」这一事实来为「正态性假设」辩护 [8]。[2] 也提出同样的质疑：高斯设定的准则是「最大似然估计应该导出优良的算术平均」，但算术平均的优良性当时更多是经验直觉，缺乏严格理论支持；于是「因为算术平均是优良的，推出误差必须服从正态分布；反过来，又基于正态分布推导出最小二乘法和算术平均来说明其优良性」，陷入了鸡生蛋蛋生鸡的怪圈 [2]。

[8] 给出了一个化解方案：如果只把 1809 年的处理视为「在误差已知为正态分布时才使用该方法的正当性说明」，循环论证就消失了。而在 1821 年的工作中，高斯放弃了正态误差函数假设，转而「运用数学概率来评估不确定性并作出推断」以论证最小二乘法 [8]。这一转向说明高斯本人也在回应这一问题。

## 「正态分布该归功于谁」

多份来源一致强调：钟形曲线的历史并非始于高斯 [1][14][15]。

- **de Moivre（1733）**：法国数学家 [[棣莫弗]] 研究「抛掷公平硬币多次后正面出现指定次数的概率」时发现，随着抛掷次数增大，二项分布趋近于一条平滑连续曲线，即钟形曲线。但他把它看作计算捷径，而非自然界的根本规律 [14]。文献常表述为「de Moivre 最早发现了正态分布」 [15]。
- **Laplace（19 世纪初）**：扩展了 de Moivre 的工作，证明今日所称的中心极限定理——许多独立随机变量之和趋于正态分布，与原变量各自的形状无关 [14]。1810 年读过高斯的工作之后，Laplace 用中心极限定理为大样本下最小二乘法与正态分布提供了辩护 [9]。
- **Euler（1748）**：Krus (2001) 主张，历史学家可以承认高斯在**阐释正态分布的性质**并把它应用于天文学方面的主导地位，但很难承认他在**描述其一般解析形式**上的优先权；Euler 在《Introductio in analysin infinitorum》（1748）中已给出该函数的解析形式。作者还引用了 Laplace 常对学生说的那句「Lisez Euler, lisez Euler, c'est notre maître à tous」（读欧拉，读欧拉，他是我们所有人的老师）[13]。
- **Robert Adrain（1808）**：这位美国人与高斯在 19 世纪初同时研究类似观念，彼此并不知道对方的工作；Adrain 在 1808 年提出正态分布可用于描述测量误差分布，其动因来自测量（surveying）中的一个实际问题，并在此基础上进一步发展与证明了 Legendre 的最小二乘法 [11]。
- **Gauss（1809）**：[11] 指出高斯 1809 年发表的工作同时包含**最大似然参数估计、最小二乘法和正态分布**几项关键贡献，这或许正是后人倾向于把功劳归于高斯的部分原因。

因此，「高斯分布」这一冠名反映的是**应用与性质阐释上的影响力**，而不是数学形式的首次出现 [13]。

## 命名与遗产

- 高斯拓展的最小二乘法成为 19 世纪统计学最重要的成就，其在 19 世纪统计学中的地位，相当于 18 世纪的微积分之于数学 [2]。
- 该方法是今日回归分析、误差分析、轨道确定、机器学习、大地测量与信号处理的基础 [7]，并被广泛用于数据建模、统计学、经济学、工程学与物理学 [7]。
- 后世德国钞票与硬币以正态密度曲线来纪念高斯，足见这项工作在当代科学发展中的分量 [2]。据 [2]，高斯去世前要求在自己的墓碑上雕刻正十七边形，以说明他在正十七边形尺规作图上的杰出工作。

## 矛盾、疑点与空白

1. **发明权归属**：最小二乘法的发表优先权属于 Legendre（1805），高斯声称 1794/1795 年已在使用但未发表 [6][9]。现有来源均未给出能裁定此争端的原始证据。
2. **正态分布优先权**：来源之间口径不同——[1] 说高斯不是最先发现者，[15] 说 de Moivre 最早发现，[13] 更把解析形式的优先权判给 Euler。这些说法指向的是不同意义上的「优先权」（发现、解析形式、性质阐释），需要在引用时严格区分。
3. **循环论证**：1809 年的推导是否构成循环，取决于如何理解该推导的定位（「辩护」还是「刻画」）[8]。这是一个仍未完全平息的解释性争论。
4. **待核实的归属**：[12] 称高斯「还提出了相关系数的概念」。这一说法与统计学史的主流叙述（相关系数通常与 Galton、Pearson 相关）存在张力，而该来源为科普性质，建议不要直接采信。
5. **Ceres 观测时长**：[9] 的 40 天与 [2] 的「6 个星期」略有出入。
6. **术语的时代错位**：「BLUE」「极大似然估计」等名词均为后世的现代术语，用来概括高斯的原始表述时需要标注 [1][6][8]。

## 建议补充的来源

- 高斯 1809 年《Theoria motus corporum coelestium》原著，用以核对误差假设与极大似然论证的原始形式 [13][14]。
- 高斯 1823 年《Theoria combinationis observationum erroribus minimis obnoxiae》及 G. W. Stewart 的英译本（SIAM, 1995），是核查 Gauss–Markov 型结论与递归最小二乘的标准文本 [6]。
- Stephen Stigler 的统计学史著作，用于厘清「循环论证」批评的完整论证 [8]。
- Legendre 1805 年的原始论文，用于确证最小二乘法的首次发表形态 [6][9]。
- 关于 Laplace 中心极限定理工作的一手文献，以补足「大样本辩护」的技术细节 [9]。
- 《数学指南——实用数学手册》0.4 节中与误差、经验分布相关的条目（如 [[经验标准差]]、[[理论分布函数]]、[[正态分布检验]]），可用于把高斯的误差理论同现代手册中的统计过程对接。

## 参见

- [[正态分布]]、[[高斯钟形曲线]]、[[概率密度]]
- [[随机变量]]、[[测量序列]]、[[经验均值]]、[[经验标准差]]
- [[理论分布函数]]、[[经验分布函数]]、[[正态分布检验]]、[[概率纸]]、[[卡方拟合检验]]
- [[数理统计]]、[[数理统计中的标准过程]]
- [[棣莫弗]]

## References

1. [（科普贴）高斯与最小二乘法 - 知乎](https://zhuanlan.zhihu.com/p/356627716) — zhuanlan.zhihu.com
2. [正态分布的前世今生(上) | 统计之都](https://cosx.org/2013/01/story-of-normal-distribution-1) — cosx.org
3. [多元线性回归（高斯分布---＞最小二乘法） - 知乎](https://zhuanlan.zhihu.com/p/378967282) — zhuanlan.zhihu.com
4. [正态分布与最小二乘法-CSDN博客](https://blog.csdn.net/The_lastest/article/details/82413772) — blog.csdn.net
6. [Carl Friedrich Gauss](https://en.wikipedia.org/wiki/Carl_Friedrich_Gauss) — en.wikipedia.org
7. [Carl Friedrich Gauss: The Quiet Genius Who Transformed ...](https://mathsciencehistory.com/carl-friedrich-gauss-the-quiet-genius-who-transformed-math-astronomy-modern-science) — mathsciencehistory.com
8. [Gauss' method of least squares](https://repository.lsu.edu/cgi/viewcontent.cgi?article=3096&context=gradschool_theses) — repository.lsu.edu
9. [Least squares - Wikipedia](https://en.wikipedia.org/wiki/Least_squares) — en.wikipedia.org
11. [Normal distribution | History | Research Starters | EBSCOhost](https://www.ebsco.com/research-starters/history/normal-distribution) — ebsco.com
12. [Carl Friedrich Gauss, The Prince Of Mathematics](https://quantumzeitgeist.com/carl-friedrich-gauss) — quantumzeitgeist.com
13. [Is normal distribution due to Karl Gauss?](https://web.archive.org/web/20060210125807/http://www.visualstatistics.net/Statistics/Euler/Euler.htm) — web.archive.org
14. [Gauss and the Normal Distribution - Kronecker Wallis](https://www.kroneckerwallis.com/gauss-and-the-normal-distribution-the-bell-curve-that-rules-statistics) — kroneckerwallis.com
15. [7: Normal Distribution](https://stats.libretexts.org/Bookshelves/Introductory_Statistics/Introductory_Statistics_(Lane)/07%3A_Normal_Distribution) — stats.libretexts.org

## Related
- [[queries/research-高斯gauss尚无论述页面-2026-09-27-031756-research-8]]
- [[queries/research-为什么许多测量值服从正态分布中心极限定理与误差理论-2026-09-27-031835-research-10]]
