---
type: query
title: "Research: t 分布与 χ² 分布的历史来源（Student、Pearson）在本节中缺失"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: t 分布与 χ² 分布的历史来源（Student、Pearson）在本节中缺失

# t 分布与 χ² 分布的历史来源：Student 与 Pearson（本节缺失内容补全）

## 概述

《数学指南——实用数学手册》6.3.2 节「重要的估计量」[[10-数学指南实用数学手册--10-632-重要的估计量--4fkaou]] 以定义—性质—公式的方式引入了 [[t分布|t 分布]]、[[卡方分布|χ² 分布]]，并给出 [[方差的估计量S2|方差的估计量 S²]] 及其 [[自由度|自由度]] $m = n - 1$ 等结论 [[632节期望与方差的估计量及其抽样分布]]。该节并未交代这两个分布的来源与命名经过，读者只能把它们当作现成的数学对象接受。

本页依据外部文献，补全 t 分布与 χ² 分布的历史背景：t 分布由 Guinness 啤酒厂的 William Sealy Gosset 以笔名 **Student** 引入，后经 [[费希尔|费希尔（R. A. Fisher）]] 完整推导并改称 $t$；χ² 分布及其拟合优度检验则源自 [[数学指南-实用数学手册|皮尔逊（Karl Pearson）]] 1900 年的论文。理解这些来源，直接关系到本节中「为什么用 $n-1$」「$t$ 与 $z$ 的关系为何是 $z = t/\sqrt{n-1}$」等具体问题。

## Student 与 t 分布

### William Sealy Gosset 其人

William Sealy Gosset（1876 年 6 月 13 日生于 Canterbury，1937 年 10 月 16 日卒）是英国统计学家、化学家和酿酒师，长期供职于都柏林的 Guinness 啤酒厂 [1]。他 1899 年毕业后即加入 Arthur Guinness & Son，此后 38 年的职业生涯全部在 Guinness 度过 [1]。其岗位包括学徒酿酒师、实验酿酒主管、统计主管，并于 1935 年升任总酿酒师（Head Brewer）直至去世 [4]。

1904 年，Gosset 为 Guinness 撰写了一份内部报告《The application of the law of error to work of the brewery》，讨论观察次数与可能误差的关系，并注意到随着样本量减小，「表示误差频率的曲线变得更高、更窄」——这正是小样本分布偏离正态分布的直观起点 [1][4]。由于 Guinness 后来规定公司研究人员的公开发表不得提及啤酒、Guinness 或作者真名，Gosset 被迫匿名发表 [1][4]。他的笔名 "Student" 很可能取自其 1906–1907 年间使用的笔记本《The Student's Science Notebook》[1][4]；其 21 篇论文中有 19 篇以 Student 之名发表 [4]。这直接导致今日通行的名称是「Student 的」而非「Gosset 的」t 分布与显著性检验 [1]。

### 1908 年论文与小样本问题

当时统计学界的主流看法是，研究者需要非常大的样本量才能可靠地估计总体 [2]。Gosset 在酿酒质控中却必须用小样本得出可外推的结论，他发现小样本下样本均值的分布并不服从正态分布，因而无法直接套用基于正态分布的传统方法 [4]。

他于 1908 年在皮尔逊主编的 *Biometrika* 上发表《The probable error of a mean》[1][4]。论文中他部分地推导了误差分布，并沿用当时记号称之为 $z$，给出了 $n = 4$ 至 $10$ 的 $z$ 值表；由于计算量庞大，表格用机械计算器耗时约六个月才完成 [4]。该文最初只覆盖到 $n = 4$，Gosset 后来解释说：「我停在 $n = 4$，因为我没有想到会有人愚蠢到用更少观测数得出的可能误差去工作」[4]。1917 年他把 $z$ 表扩展到 $n = 2$ 至 $30$ [4]。

### 从 z 到 t：费希尔的角色

Gosset 与皮尔逊关系良好，后者帮他处理论文中的数学，包括 1908 年的那批论文，但对这些小样本工作的重要性评价并不高 [1]。真正认识到其价值的是 [[费希尔|费希尔]]：他于 1912 年致信 Gosset，指出 Student 的 $z$ 分布应当以自由度而非总样本量 $n$ 作除数 [1]。1912 至 1934 年间两人通信超过 150 封；1924 年 Gosset 在信中写道：「我给你寄一份 Student 的表，因为你是唯一一个可能用到它的人！」[1][4]

1925 年，费希尔发表论文完整推导了 Student 分布，并将其表述为一个变换后的正态分布；他把记号由 $z$ 改为 $t$，把参数由 $n$ 改为 $(n-1)$ 即自由度 [4]。同年 *Metron* 特刊中，Student 发表了修正后的表，即今日所称的 Student's $t$，其与旧 $z$ 的换算关系为

$$z = \frac{t}{\sqrt{n-1}}$$

费希尔在同一卷中还给出了 $t$ 分布在回归分析中的应用 [1]。值得注意的是，Gosset 本人对用 $n-1$ 仍有保留：「当数目很小时，我认为我们用的公式（含 $n-1$）更好，但若 $n$ 大于 10，差别小到不值得多费这份事」[4]。尽管如此，他到 1917 年已在表中使用 $(n-1)$ [4]。

## Karl Pearson 与 χ² 分布

χ² 分布与拟合优度检验出自皮尔逊 1900 年的论文《On the criterion that a given system of deviations from the probable in the case of a correlated system of variables is such that it can be reasonably supposed to have arisen from random sampling》，发表于 *Philosophical Magazine* 第 5 系列第 50 卷第 302 期，第 157–175 页 [7]。该文引入了后来被称为 χ² 拟合优度检验（chi-squared test of goodness of fit）的方法 [6][8]。

据文献评述，皮尔逊是第一个识别出该问题并引入相应准则的人 [8]；这是历史上第一个可适用于任意形状曲线的拟合优度检验的数学表述 [10]。在论文中，皮尔逊把 χ² 统计量表述为「a measure of goodness of fit」，且该统计量本身出现在分布函数的指数位置上 [9]。需要指出的是，皮尔逊 1900 年论文所用的术语与暗示距今已逾百年，对现代读者构成阅读障碍，其检验程序的解释与成就评估并不像表面上那样直截了当 [6]。

## 自由度与 n − 1 的由来

本节中反复出现的 $n-1$ 除数，其历史线索有两方面。其一是统计学中的 **Bessel 校正**：在样本方差与样本标准差公式中用 $n-1$ 而非 $n$ 作除数 [13]。该修正补偿了因用样本均值代替总体均值而损失的一个自由度，使样本方差成为 [[估计量的无偏性|无偏估计]] [14]。其二是费希尔 1912 年对 Gosset 的建议——$z$ 应以自由度而非 $n$ 作除数 [1]。两条线索指向同一现象，即小样本中自由度被消耗一个的处理方式；本节在 [[方差的估计量S2|方差的估计量 S²]] 与 [[自由度|自由度]] 条目下给出的是结论，而未交代这一处理的历史动因。

## 本节缺失的内容及其影响

综合上述文献，6.3.2 节的缺口可概括为以下几点：

1. **命名与来源缺失**：t 分布、χ² 分布作为现成对象给出，未提及 Gosset（Student）、皮尔逊、费希尔，读者无从知晓其统计实践背景（啤酒厂质控、小样本问题）[1][4]。
2. **记号演变缺失**：t 分布原称 $z$ 分布，1925 年费希尔才改称 $t$ 并引入自由度 $n-1$；缺少 $z = t/\sqrt{n-1}$ 的关系，会削弱对分布参数化方式的理解 [1][4]。
3. **自由度 $n-1$ 的动因缺失**：Bessel 校正的无偏性动机与费希尔关于自由度的建议均未出现 [1][13][14]。
4. **χ² 与拟合优度检验的关联缺失**：本节只给出 χ² 分布本身，未说明它最初是作为拟合优度检验的准则而引入的 [6][8][10]。
5. **人物关系网缺失**：皮尔逊—Gosset—费希尔之间既有合作（皮尔逊帮 Gosset 处理数学、主编其 1908 年论文）又有分歧（费希尔与 Gosset 长期争论平衡设计与随机化设计、显著性阈值）[1][4]。

## 矛盾与待核实之处

- **笔名来源为推测性表述**：来源 [1] 用 "may have taken"，[4] 用 "apparently"，均非确证，笔名 "Student" 是否确实取自《The Student's Science Notebook》尚待原始文献佐证。
- **期刊名拼写不一致**：来源 [1] 写作 *Biometrika*，[4] 同一刊物写作 *Biometrica*；通行拼写为 *Biometrika*，[4] 处疑为笔误。
- **费希尔介入时间线**：来源 [1] 称 1912 年费希尔已指出应以自由度作除数，来源 [4] 则称 1912 年仅是通信开始、1925 年才给出完整推导。二者并不必然冲突（早期建议 vs. 完整推导），但需明确区分「提出」与「完成」两个节点。
- **来源 [2] 文本残缺**：该来源（usu.edu）正文存在明显断句与缺文，不宜作为主要依据，仅可作旁证。
- **χ² 分布中「自由度」概念的确立时间**：皮尔逊 1900 年论文是否已明确自由度概念，所收来源未给出细节，需查原文 [7]。

## 建议补充的来源

- Student (1908). *The probable error of a mean*. *Biometrika*.
- Student (1917). 扩展后的 $z$ 分布表（$n = 2$ 至 $30$）。
- Fisher, R. A. (1925). 完整推导 Student 分布的论文，以及 *Metron* 特刊中的回归应用。
- Pearson, K. (1900). *Philosophical Magazine*, Series 5, **50**(302): 157–175. doi:10.1080/14786440009463897（χ² 拟合优度检验原始论文）。
- Plackett, R. L. *Karl Pearson and the Chi-Squared Test*, JSTOR 编号 1402731（对皮尔逊 1900 年论文的现代评述）。
- Ziliak, Stephen T. (2008). *Retrospectives: Guinnessometrics: The Economic Foundation of "Student's" T*. *Journal of Economic Perspectives*, **22**(4): 199–216. doi:10.1257/jep.22.4.199。
- MacTutor History of Mathematics Archive, "William Sealy Gosset"（University of St Andrews）。
- Ziliak (2019) 关于 Gosset 与费希尔在平衡设计、随机化设计与显著性阈值上长期分歧的研究。

另可对照本 wiki 中 [[t检验|t 检验对两均值的比较]]、[[F分布|F 分布]]、[[正态分布期望的置信区间|正态分布期望的置信区间]]、[[正态分布标准差的置信区间|正态分布标准差的置信区间]]、[[伽马函数|伽马函数]] 等条目，检查这些分布族在各处的历史表述是否一致，以及是否同样需要补注来源。

## References

1. [William Sealy Gosset - Wikipedia](https://en.wikipedia.org/wiki/William_Sealy_Gosset) — en.wikipedia.org
2. [William Sealy Gosset](https://www.usu.edu/math/schneit/StatsHistory/ModernStatisticians/Gosset) — usu.edu
4. [The strange origins of the Student's t-test - The Physiological Society](https://www.physoc.org/magazine-articles/the-strange-origins-of-the-students-t-test/) — physoc.org
6. [Karl Pearson and the Chi-Squared Test - jstor](https://www.jstor.org/stable/1402731) — jstor.org
7. [Pearson's chi-squared test - Wikipedia](https://en.wikipedia.org/wiki/Pearson%27s_chi-squared_test) — en.wikipedia.org
8. [Karl Pearson Chi-Square Test The Dawn of Statistical Inference](https://link.springer.com/chapter/10.1007/978-1-4612-0103-8_2) — link.springer.com
9. [How did Karl Pearson come up with the chi-squared statistic?](https://stats.stackexchange.com/questions/97604/how-did-karl-pearson-come-up-with-the-chi-squared-statistic) — stats.stackexchange.com
10. [Karl Pearson, paper on the chi square goodness of fit test (1900)](https://www.researchgate.net/publication/285963043_Karl_Pearson_paper_on_the_chi_square_goodness_of_fit_test_1900) — researchgate.net
13. [Bessel's correction - Wikipedia](https://en.wikipedia.org/wiki/Bessel%27s_correction) — en.wikipedia.org
14. [[PDF] On Bessel's Correction: Unbiased Sample Variance, the Bariance ...](https://thescipub.com/pdf/jmssp.2025.44.49.pdf) — thescipub.com

## Related
- [[queries/research-t-分布χ2-分布与-n1-校正的历史来源缺失-2026-09-27-161911-research-65]]
