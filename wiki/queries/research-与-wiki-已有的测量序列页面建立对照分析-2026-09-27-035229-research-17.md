---
type: query
title: "Research: 与 wiki 已有的测量序列页面建立对照分析"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 与 wiki 已有的测量序列页面建立对照分析

# 与 wiki 已有的测量序列页面建立对照分析

## 引言

本页把新收集的英文统计学文献（围绕 **t 检验自由度 degrees of freedom, df**、**汇总方差 pooled variance**、**Welch's t-test** 等主题）与 wiki 中既有的 [[测量序列]] 系列页面进行对照。后者主要源自《数学指南——实用数学手册》0.4 节，核心页面包括 [[10-数学指南实用数学手册--15-045-两个测量序列的统计比较--1xbqvrd]]（0.4.5 两个测量序列的统计比较）与 [[10-数学指南实用数学手册--13-044-测量序列的统计计算--onnmc5]]（0.4.4 测量序列的统计计算），并派生出一批 [[t检验]]、[[自由度]]、[[f检验]]、[[威尔科克森检验]] 等概念页与 findings 页。

对照的目的不是重复公式，而是**检验两套材料在关键统计约定上是否自洽**，并据此指出 wiki 中可能存在的转写疑误或约定差异。

---

## 一、研究来源的核心内容

### 1.1 单样本 t 检验

单样本 t 检验把样本均值与已知总体均值作比较，自由度为

$$df = n - 1$$

例如 n = 30 时 df = 29 [1]。这一约定在文献中高度一致 [2][4]。

### 1.2 独立双样本 t 检验（等方差假设）

当假定两组总体方差相等时，使用**汇总方差**（pooled variance）：

$$\hat{\sigma}^2_{pooled} = \frac{(n_1-1)\hat{\sigma}_1^2 + (n_2-1)\hat{\sigma}_2^2}{n_1 + n_2 - 2}$$

对应自由度为

$$df = n_1 + n_2 - 2$$

当 $n_1 = n_2 = n$ 时该式退化为 $2n - 2$ [2][3][5]。注意加权特性：$n$ 较大的一组其 $s^2$ 在汇总估计中权重更大 [3]。

### 1.3 Welch's t 检验（不等方差假设）

当不假定方差相等时使用 Welch's t-test（又称 unequal variances t-test），自由度为 **Welch–Satterthwaite 方程**给出的分数自由度：

$$df = \frac{\left(\dfrac{s_1^2}{n_1} + \dfrac{s_2^2}{n_2}\right)^2}{\dfrac{\left(s_1^2/n_1\right)^2}{n_1 - 1} + \dfrac{\left(s_2^2/n_2\right)^2}{n_2 - 1}}$$

该值通常非整数，使用时四舍五入为整数 [1][2][5]。Welch 检验可视为 **Behrens–Fisher 问题的近似解**，其自由度一般**小于** Student 检验所用的 df [6][9]。

### 1.4 保守做法

一种简化的保守方法直接取

$$df = \min(n_1 - 1,\ n_2 - 1)$$

代价是置信区间更宽、假设检验更保守 [1]。

### 1.5 方法学争论

多篇来源主张**默认使用 Welch's t-test**：在方差或样本量不等时它比 Student 检验更优，而在两者相等时结果一致 [10]。广为推荐的「先用 Levene's test 检验方差齐性、再二选一」的两步法被批评为不可取，原因是 Levene 检验功效常偏低，容易错误地接受方差相等假设 [7][10]。R 与 Minitab 等软件已默认输出 Welch 检验 [7]。

---

## 二、与 wiki 已有页面的逐项对照

### 2.1 自由度记号与单样本情形

wiki 的 [[自由度]] 采用记号 $m = n - 1$，与文献中的 $df = n - 1$ 完全一致。[[10-数学指南实用数学手册--13-044-测量序列的统计计算--onnmc5]] 中关于 [[均值的置信限]] 与 [[标准差与方差的置信区间]] 的构造，也以 $m = n - 1$ 为基础，并借助 [[t-alpha-m分位数]]、[[卡方分位数]] 完成。**这一层面两套材料自洽**，并共同依赖 [[正态分布]] 假设。

### 2.2 双样本情形：关键分歧

wiki 的 [[t检验]] 页面描述「t 检验对两均值的比较」，配 [[药物A]] 与 [[药物B]] 的治愈时间例，并产生了 findings [[药物A与B治愈时间均值存在重要差别]] 与 [[药物A与B治愈时间标准差实质相同]]。然而，wiki 内部已存在一条悬而未决的疑问：

> [[t检验自由度m为何取n1加n2减1]]

即手册在双样本比较中似乎采用 $m = n_1 + n_2 - 1$，而本轮收集的全部文献一致采用 $m = n_1 + n_2 - 2$ [1][2][3][4][5]。这是本次对照中**最突出的矛盾**，详见第三节。

### 2.3 方差齐性检验：F 检验与 Levene 检验

wiki 的 [[f检验]] 被定义为「方差比检验」，用于判断两组 [[经验标准差]] 是否实质相同；这正是 findings [[药物A与B治愈时间标准差实质相同]] 所依赖的判据。对照文献可见：

- 数学上，方差齐性检验对应 F 检验（两方差之比）；
- 而在现代应用统计中，更常被讨论的是 **Levene's test**[7][10]，它正是「两步法」中被质疑功效不足的那一步；
- 文献主流意见倾向于**跳过方差预检验、直接采用 Welch 检验**[7][9][10]，这与 wiki 手册「先做 F 检验、再做 t 检验」的流程存在方法论取向上的差异。

wiki 另有 [[f检验误差概率为002的来源]] 与 [[queries/威尔科克森检验内容依赖6.3.4.5]] 两条未决疑问，说明 0.4.5 的双样本流程本身尚待补全。

### 2.4 非参数替代：威尔科克森检验

当正态性假设不满足时，文献建议转向非参数方法 [6][11]；wiki 对应的页面为 [[威尔科克森检验]]，与 [[威尔科克森]] 相关联。两套材料在此**方向一致**，但 wiki 的威尔科克森检验内容依赖手册 6.3.4.5，尚未完整入库。

### 2.5 软件与实践落地

[[10-数学指南实用数学手册--15-03-数学与计算机数学中的革命--1abq9h3]] 与 0.4 节曾推荐 [[spss]]、[[sas]] 等工具。文献 [7] 指出 SPSS、R、Minitab 等在对 t 检验的默认设定上已普遍转向 Welch；这与 wiki 中 [[04节统计软件推荐的时效性]] 所关注的时效性问题相互印证。

---

## 三、矛盾与差异汇总

| 项目 | 研究文献约定 | wiki 既有约定 | 状态 |
|---|---|---|---|
| 单样本自由度 | $n - 1$ [1][2] | $m = n - 1$（[[自由度]]） | 一致 |
| 双样本等方差自由度 | $n_1 + n_2 - 2$ [1][2][3][4][5] | 疑为 $m = n_1 + n_2 - 1$（[[t检验自由度m为何取n1加n2减1]]） | **矛盾** |
| 不等方差自由度 | Welch–Satterthwaite 分数 df [1][2] | 未见对应条目 | **空白** |
| 方差齐性判定流程 | 直接默认 Welch [7][10] | 先 F 检验再 t 检验（[[f检验]]） | **取向差异** |
| 非参数替代 | Wilcoxon / Welch [6][11] | [[威尔科克森检验]]（依赖 6.3.4.5） | 待补全 |

**关于最突出的分歧**：如果 wiki 手册确实写作 $m = n_1 + n_2 - 1$，可能有三种解释——(a) 转写讹误（应为 $n_1 + n_2 - 2$）；(b) 手册采用了某种特定（非常规）的参数化或配对处理；(c) 该例实际为**配对样本**（paired samples）而非独立样本，此时自由度约定不同 [12][15]。在缺少 0.4.5 原始正文与表格的情况下，无法定论，故该疑问应继续保留为开放问题。

---

## 四、空白与待补充

1. **Welch's t-test 尚未在 wiki 中建立任何概念页**。建议新增 [[queries/概念-welch-t-检验]]，收录 Welch–Satterthwaite 方程，并与 [[t检验]]、[[自由度]] 互链。
2. **0.4.5 表格与正文缺失**：[[queries/0.4.6.3与0.4.6.5表格引用在本wiki中缺失]] 与 [[queries/威尔科克森检验内容依赖6.3.4.5]] 表明双样本流程的判据表尚未入库，直接导致无法核对 $m = n_1 + n_2 - 1$。
3. **配对样本与独立样本的区分**在现有 wiki 中未见独立页面，而文献 [12][15] 明确把 matched/paired samples 列为独立类别。
4. **Levene's test** 无对应条目，与 [[f检验]] 的关系尚未厘清。
5. **类型 I / 类型 II 错误率**（Type I / Type II error rate）与 [[误差概率]] 的对应关系可进一步梳理 [6][7]。

---

## 五、建议补充的来源

- **原始手册 0.4.5 正文与判据表**：用以确认 $m = n_1 + n_2 - 1$ 是原文约定还是转写讹误（优先级最高）。
- **Bernard Lewis Welch 原始论文**（1947, *Biometrika*）：为 [[queries/概念-welch-t-检验]] 提供一手来源。
- **Behrens–Fisher 问题**的专门条目：解释 Welch 方法的适用边界 [9]。
- **Levene's test 与 Brown–Forsythe test** 的条目：补足方差齐性检验谱系。
- **Delacre et al. (2017)** 等推荐 Welch 的实证文献：对应 [7][10] 的论据。
- **手册 6.3.4.5**：补全 [[威尔科克森检验]] 的完整流程。
- **配对样本 t 检验**的标准来源，用于排查 wiki 双样本例是否为配对设计 [12][15]。

---

## 结论

两套材料在**单样本自由度**、**正态性假设**、**非参数替代方向**上彼此吻合，共同支撑 wiki 的 [[测量序列]]、[[经验均值]]、[[经验标准差]] 基础体系。主要张力集中在**双样本 t 检验的自由度约定**（$n_1 + n_2 - 1$ 对 $n_1 + n_2 - 2$）以及**是否应当先做方差齐性预检验**这两个问题上。前者更像一处待核实的转写问题（见 [[t检验自由度m为何取n1加n2减1]]），后者则是应用统计界的真实方法论分歧。在 0.4.5 原始表格入库之前，本页的对照结论应视为**初步的、可被修正的**。

## References

1. [Degrees of Freedom](https://stattrek.com/statistics/degrees-of-freedom) — stattrek.com
2. [Two-sample t-tests](https://people.umass.edu/bwdillon/files/linguist-609-2020/Notes/TwoSampleT-Test.html) — people.umass.edu
3. [4.2: Pooled Two-sampled t-test (Assuming Equal Variances) - Statistics LibreTexts](https://stats.libretexts.org/Bookshelves/Applied_Statistics/Natural_Resources_Biometrics_(Kiernan)/04%3A_Inferences_about_the_Differences_of_Two_Populations/4.02%3A_Pooled_Two-sampled_t-test_(Assuming_Equal_Variances)) — stats.libretexts.org
4. [Two sample student t test](https://rpubs.com/Mabad12/987373) — rpubs.com
5. [Hypothesis Testing: Two sample mean](https://www.andrews.edu/~calkins/math/edrm611/edrm10.htm) — andrews.edu
6. [13.4: The Independent Samples t-test (Welch Test) - Statistics LibreTexts](https://stats.libretexts.org/Bookshelves/Applied_Statistics/Learning_Statistics_with_R_-_A_tutorial_for_Psychology_Students_and_other_Beginners_(Navarro)/13%3A_Comparing_Two_Means/13.04%3A_The_Independent_Samples_t-test_(Welch_Test)) — stats.libretexts.org
7. [Why Psychologists Should by Default Use Welch’s t-test Instead of Student’s t-test | International Review of Social Psychology](https://rips-irsp.com/articles/10.5334/irsp.82) — rips-irsp.com
9. [Welch's t-test - Wikipedia](https://en.wikipedia.org/wiki/Welch%27s_t-test) — en.wikipedia.org
10. [The 20% Statistician: Always use Welch's t-test instead of Student's t-test](http://daniellakens.blogspot.com/2015/01/always-use-welchs-t-test-instead-of.html) — daniellakens.blogspot.com
11. [Two-sample hypothesis testing - Wikipedia](https://en.wikipedia.org/wiki/Two-sample_hypothesis_testing) — en.wikipedia.org
12. [10: Hypothesis Testing with Two Samples - Statistics LibreTexts](https://stats.libretexts.org/Courses/Los_Angeles_City_College/Introductory_Statistics/10%3A_Hypothesis_Testing_with_Two_Samples) — stats.libretexts.org
15. [Statistics for Business Study Guide: Hypothesis Testing & ANOVA | Notes](https://www.pearson.com/channels/business-statistics/study-guides/comparing-means-and-proportions-two-sample-tests) — pearson.com

## Related
- [[queries/research-威尔科克森检验的完整方法内容手册-6345-2026-09-27-035157-research-16]]
