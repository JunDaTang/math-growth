---
type: query
title: "Research: 误差传播与 GUM/JCGM 测量不确定度框架的对照"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 误差传播与 GUM/JCGM 测量不确定度框架的对照

# 误差传播与 GUM/JCGM 测量不确定度框架的对照

## 概述

经典的“误差传播”（error propagation）与当代计量学所采用的 GUM/JCGM 测量不确定度框架，是处理“测量结果有多可靠”这一问题的两种范式。前者以误差（error）为核心量，通常通过对测量函数的微分（或差分）把各分量的误差限线性叠加；后者以不确定度（uncertainty）为核心量，把每一个影响量视为一个概率分布，通过方差合成得到合成标准不确定度，并可进一步给出扩展不确定度 [10][11][13]。

本文的目的不是重复 GUM 的操作步骤，而是把两套语言并置对照，指出它们在术语、数学结构、输入评定方式和结果表达上的差异，并标注现有资料中的矛盾与空缺。需说明的是，本 wiki 既有页面集中于《数学指南——实用数学手册》的复分析、偏微分方程等数学内容，尚无任何页面覆盖计量学与测量不确定度，因此本文不产生指向既有页面的 [[wikilink]]，而构成该主题在本 wiki 中的首批条目之一。

## 术语辨析：误差与不确定度

多个来源一致强调：“误差”与“不确定度”不是同义词，尽管常被混用 [6][7][10]。

- **误差**被定义为测量结果与被测量真值之差 [7][8][9]。它是一个“数值差”，指向一个具体的（但通常未知的）偏离量。
- **不确定度**则被描述为对测量结果可靠性的刻画，是“真值可能落入的区间”的估计，其本质是一个概率分布的度量 [6][7][10]。

FIDUCEO 给出了一个关键的逻辑论证：由于我们永远无法知道被测量的“真值”，也就永远无法知道误差的具体取值；因此误差本身是不可知的，只能把它描述为从某个概率分布中的一次抽样，而**标准不确定度正是该分布的标准差** [10]。这一论证把“误差”从可计算的量降格为不可观测量，同时把“不确定度”提升为可直接评定、可报告的量。

一个常被引用的直观例子来自电阻测量：若某材料电阻的公认值为 3.4 Ω，两次测得 3.35 Ω 与 3.41 Ω，则各次与公认值之差是误差，而两次测量值之间的跨度 0.06 Ω（即 0.06 Ω 的范围）可被视为不确定度范围的体现 [6]。更细的定性表述是：误差回答“这次测量偏了多少”，不确定度回答“我们对这个结果能信到什么程度” [7]。

> **注意（潜在混淆）**：来源 [6] 进一步给出“绝对不确定度约为区间半宽，即 (9.9−9.6)/2 = 0.15 m/s²”的重力加速度示例。这属于对“不确定度 = 半极差”的启发性近似，与 GUM 把标准不确定度定义为分布标准差的做法**并不等价**；只有当分布为均匀分布时，半宽与标准差之间才存在固定比例关系。阅读时应把 [6] 视为科普性解释，而非 GUM 定义。

## GUM/JCGM 文档体系

GUM 并非单份文件，而是一套由 BIPM 下属的 **JCGM**（Joint Committee for Guides in Metrology，计量学指南联合委员会）发布与维护的文档组合 [1][2]：

- **2017 年**，JCGM 对其由第 1 工作组（Working Group 1）编制或拟编制的文档进行了重新命名，整套文档统称为 “Guide to the expression of uncertainty in measurement”，即 **GUM**；其中单一部分以对应的 JCGM 编号指称（例如 GUM 第 6 部分为 **JCGM GUM-6:2020**）[2]。
- **JCGM GUM-1:2023**（“Part 1: Introduction”）是该套文档的导论部分，取代了 **JCGM 104:2009**，介绍各流程并索引后续各部分 [2]。
- **JCGM 100:2008** 是该体系的核心，标题为 “Evaluation of measurement data — Guide to the expression of uncertainty in measurement”，提供评定与表达测量不确定度的一般规则 [2][3]。该文件亦被重新指定为 **ISO/IEC Guide 98-3** [13]。
- **ISO/IEC Guide 98-1:2009**（“Uncertainty of measurement — Part 1: Introduction”）是 GUM 的简要导论，用于说明该基础性指南的相关性、推动其应用，并勾勒出旨在把 GUM 扩展到更广泛领域的问题的相关文件 [4]。

历史上，GUM 源于 **ISO/TAG 4/WG 3** 的工作，于 **1993 年**由 ISO 以七个支持其发展的国际组织之名义出版（1995 年更正并重印），全文约 100 页 [5]。其适用范围被明确设定为“从车间到基础研究”（from the shop floor to fundamental research），覆盖质量控制与质量保证、法规符合性与执法、科学与工程的基础与应用研究、计量标准与仪器的校准与测试、以及国家与国际物理参考标准的研制与比对等 [3]。GUM 也适用于实验、测量方法以及复杂部件与系统的概念设计和理论分析，此时“测量结果”可完全是概念性的、基于假设数据 [2][3]。

值得强调的是，GUM 给出的是**一般规则而非分技术领域的详细规程**，且不讨论某一测量结果的不确定度在评定之后可以如何被用于不同目的（例如判断该结果与其他类似结果的相容性）[3]。

## GUM 框架的核心方法

### 测量模型与被测量

GUM 的首要关切是“被测量”（measurand）——一个可由本质上唯一的值刻画的、定义良好的物理量——的不确定度表达 [3]。若所关心的现象只能表示为值的分布，或依赖于时间等参数，则用于描述它的被测量即为描述该分布或该依赖关系的那组量 [3]。

### A 类与 B 类评定

来源 [13] 指出，每次测量都受到多个误差源的影响——抽样、仪器分辨力、校准不确定度、操作者手法等——GUM 提供了一种有纪律的方式把它们合成单一数字。FIDUCEO 也提到测量不确定度存在两种评定方式，其详细信息见 GUM 以及 NPL 的 “Uncertainty Analysis for Earth Observation” 电子学习课程 [10]。其中**灵敏系数**（sensitivity coefficients）被称为不确定度评定的一个关键组成 [10]。

### 不确定度传播律与合成标准不确定度

GUM 的核心运算通常被称为“不确定度传播律”（law of propagation of uncertainty）。按 **JCGM 100:2008 §5.1.2（公式 11）**，**合成标准不确定度**（combined standard uncertainty）$u_c$ 是合成方差的**正平方根**，即各输入量方差与协方差之和的平方根 [11][14]。在一个教学性的简化假设下——即所有分量已用与被测量相同的单位表达——$u_c$ 退化为各分量标准不确定度的方和根 [13]：

$$u_c = \sqrt{\textstyle\sum_i u_i^2}$$

每个分量的方差 $u_i^2$ 除以总方差，即给出该分量在合成不确定度中所占的份额，这正是“贡献分解”（contribution breakdown）所显示的内容 [13]。

### 扩展不确定度与包含因子

**扩展不确定度**（expanded uncertainty）$U$ 由合成标准不确定度乘以**包含因子**（coverage factor）$k$ 得到，即 $U = k\,u_c$ [14]。来源 [1] 强调 GUM 在结果表达上主张使用置信区间、扩展不确定度与包含因子，并要求不确定度与测量值一并报告，以标明与该测量相关联的置信水平，从而让数据使用者能判断结果的可靠性与准确度。[13] 给出的教学计算器同样以 $k=2$ 为例给出扩展不确定度。

### 不确定度预算与结果报告

GUM 实践中的一个标准工具是**不确定度预算**（uncertainty budget）：列出各来源、其类型（A 类或 B 类）与标准不确定度，然后按方和根合成 [1][13]。报告格式方面，JCGM 100:2008 给出多种规范写法 [12]：

1. $m_S = 100{,}021\ 47\ \text{g}$，合成标准不确定度 $u_c = 0{,}35\ \text{mg}$；
2. $m_S = 100{,}021\ 47(35)\ \text{g}$，括号内数字为 $u_c$ 相对于所引结果末位数字的数值；
3. $m_S = 100{,}021\ 47(0{,}000\ 35)\ \text{g}$，括号内数字为以所引结果单位表示的 $u_c$；
4. $m_S = (100{,}021\ 47 \pm 0{,}000\ 35)\ \text{g}$，其中 $\pm$ 号后的数字是 $u_c$ 的数值，**而非置信区间**。

文件本身提示：$\pm$ 格式应尽可能避免，因为它在传统上容易被误读为置信区间 [12]。

## 算例：端度规校准与 Rockwell 硬度

JCGM 100:2008 附录 H 提供了数个完整算例 [12]：

- **端度规（end gauge）比较**：标准端度规的校准证书给出 $l_S = 50{,}000\ 623\ \text{mm}$（在 20 °C 下）；对未知端度规与标准端度规长度差的五次重复观测的算术平均为 $d = 215\ \text{nm}$。由 $l = l_S + d$ 得未知端度规在 20 °C 下的长度 $l = 50{,}000\ 838\ \text{mm}$，合成标准不确定度 $u_c = 32\ \text{nm}$，相对合成标准不确定度 $u_c/l = 6{,}4\times10^{-7}$。该例中占主导的分量显然是标准器的不确定度 $u(l_S) = 25\ \text{nm}$ [12]。
- **Rockwell C 硬度**：在假设 $\Delta c = 0$ 时，试样块的硬度为 $h_{\text{Rockwell C}} = 64{,}0$ 个 Rockwell 标度单位，或 $0{,}128\ 0\ \text{mm}$，合成标准不确定度 $u_c = 0{,}55$ 个 Rockwell 标度单位或 $0{,}001\ 1\ \text{mm}$；以硬度指数表示即 $H_{\text{Rockwell C}} = 64{,}0\ \text{HRC}$，$u_c = 0{,}55\ \text{HRC}$。除国家硬度标准机与硬度定义带来的分量 $u(\Delta_S) = 0{,}5$ 个标度单位外，显著分量还包括机器的重复性 $p(\bar{d})/k = s_p(\bar{d})/5 = 0{,}20$ 个标度单位等 [12]。

这两个算例体现了 GUM 的典型形态：先写出**测量模型**（如 $l = l_S + d$），再逐项评定输入量标准不确定度，最后按 §5.1.2 合成 [12]。

## 误差传播与 GUM 框架的对照

| 维度 | 经典误差传播 | GUM/JCGM 框架 |
|---|---|---|
| 核心量 | 误差，即结果减去真值 [7][8][9] | 不确定度，即分布的标准差 [10] |
| 可认知性 | 真值未知，故误差不可知 [10] | 不确定度可评定、可报告，是可靠性的度量 [6][7][10] |
| 数学结构 | 对测量函数作微分/差分，误差限线性叠加 | 对测量模型作一阶展开，方差与**协方差**按方和根合成（JCGM 100:2008 §5.1.2，公式 11）[11][13][14] |
| 输入评定 | 对“系统/随机”的划分常较模糊 | 明确区分 **A 类**（统计方法）与 **B 类**（其他信息）评定 [10][13] |
| 灵敏系数 | 隐含于偏导数 | 被显式提出并作为评定关键环节 [10] |
| 输出表达 | 常见形式为“结果 ± 误差限” | 标准不确定度 $u_c$ 与扩展不确定度 $U = k u_c$，附包含因子 [1][14] |
| 相关性问题 | 常假设分量独立而忽略 | 合成公式中显式含协方差项 [11][14] |
| 报告规范 | 无统一格式 | 多种规范写法；$\pm$ 格式被劝退，因其非置信区间 [12] |
| 适用层级 | 依具体领域惯例 | 自车间至基础研究的广泛谱系 [2][3] |
| 是否给出技术细节 | 视教科书而定 | 明确声明只给一般规则，不提供分技术领域的详细指令 [3] |

需要强调的是，GUM 并未“废除”误差传播的思想，而是把它重新奠基：当测量模型近似线性、各输入量不确定度足够小时，GUM 的传播律与经典误差传播在数学形式上高度相似——差别主要在于语义（误差 vs 不确定度）、对相关性/协方差的显式处理，以及一套成文的评定与报告规范 [11][13][14]。

## 矛盾、局限与空白

1. **“不确定度 = 半极差”与 GUM 定义冲突**：来源 [6] 的示例以区间半宽近似不确定度，而 GUM 体系把标准不确定度定义为分布标准差 [10]。二者仅在特定分布假设下等价，不应混用。
2. **$\pm$ 格式的地位**：实践中“结果 ± 不确定度”被广泛使用，但 JCGM 100:2008 明确劝退该格式，理由是它容易被理解为置信区间 [12]。这是一个“实践惯例 vs 规范建议”的典型张力。
3. **覆盖因子 $k$ 的取值条件**：来源仅给出 $k=2$ 的示例 [13] 与“$U = k u_c$”的表述 [14]，但未说明 $k$ 与置信水平、有效自由度（Welch–Satterthwaite 公式）之间的关系。这一空白需查原文件补齐。
4. **A 类/B 类的具体操作**：现有来源只提到存在两种评定方式 [10] 并提及“抽样、仪器分辨力、校准不确定度、操作者手法”等来源 [13]，未给出 A 类评定的自由度处理、B 类评定的分布假设选择等细节。
5. **GUM 的扩展体系**：JCGM GUM-1:2023 明确说整套文档包含多个部分 [2]，ISO/IEC Guide 98-1:2009 也表示存在把 GUM 推广到更广泛领域的相关文件 [4]，但现有来源未涉及 Monte Carlo 方法（JCGM 101）、GUM-6:2020 等内容，无法在本页展开。
6. **非线性与高阶项**：GUM 传播律建立在（近似）线性化之上 [10][11]，当模型强非线性时该近似的失效条件与替代方案在现有来源中完全缺失。
7. **本 wiki 的内嵌缺口**：既有页面全部服务于《数学指南——实用数学手册》的复分析、偏微分方程与微分方程主题，与计量学无交集。本页是该主题的孤岛式入口，尚无同主题的实体页（如 JCGM、BIPM、NIST）或概念页（如“误差传播律”“A 类评定”）可供互链。

## 建议补充的来源

为把本页从导论级提升到可操作级，建议后续检索并入库以下来源：

- **JCGM 100:2008 正文**（而非仅附录 H 摘录），特别是第 4、5、7 条关于 A 类/B 类评定、传播律的一般公式（含协方差项）、以及包含因子的讨论 [3][12]。
- **JCGM GUM-1:2023** 的附表 A.1（各部分总览），以完整刻画 GUM 套件的结构 [2]。
- **JCGM 101（用 Monte Carlo 方法传播分布）** 与 **JCGM GUM-6:2020**，用以补足非线性场景与测量模型的进一步指南 [2]。
- **ISO/IEC Guide 98-1:2009** 与 **ISO/IEC Guide 98-3** 的正文，以核实编号对应关系 [4][13]。
- **NIST 的 Uncertainty 专题页**（Basic / Evaluating / Combining / Expanded & coverage / Examples / Background），可作为教学性次级来源 [5]。
- **FIDUCEO 与 NPL 的“Uncertainty Analysis”教程**，用以补充灵敏系数与两种评定方式的操作性说明 [10]。
- **Cohen, “Error and Uncertainty in Physical Measurements”（Springer）**，用于追溯误差/不确定度区分的学理背景 [7]。
- 有关 **JCGM 200:2012（VIM，国际计量学词汇）** 的检索，用以统一术语；现有来源中“误差”定义的措辞差异（“结果减真值” [8][9] vs “结果与被测量值之差” [7]）很可能源于对 VIM 术语的不同转述。

## References

1. [Understanding GUM and Measurement Uncertainty - Interface](https://www.interfaceforce.com/understanding-gum-and-measurement-uncertainty) — interfaceforce.com
2. [[PDF] Guide to the expression of uncertainty in measurement - Part 1 - BIPM](https://www.bipm.org/documents/20126/2071204/JCGM_GUM-1.pdf) — bipm.org
3. [JCGM 100:2008 (GUM 1995 with minor corrections](https://www.bipm.org/documents/20126/2071204/JCGM_100_2008_E.pdf) — bipm.org
4. [ISO/IEC Guide 98-1:2009 - Uncertainty of measurement — Part 1: Introduction to the expression of uncertainty in measurement](https://www.iso.org/standard/46383.html) — iso.org
5. [Introduction, continued](https://physics.nist.gov/cuu/Uncertainty/international2.html) — physics.nist.gov
6. [What's meaning and difference of Uncertainty and Errors (Tolerance) - LISUN](https://www.lisungroup.com/news/technology-news/whats-meaning-and-difference-of-uncertainty-and-errors-tolerance.html) — lisungroup.com
7. [Error and Uncertainty in Physical Measurements](https://link.springer.com/chapter/10.1007/978-3-642-80199-0_8) — link.springer.com
8. [What is the difference between "Error" and "Uncertainty"?](https://physics.stackexchange.com/questions/796108/what-is-the-difference-between-error-and-uncertainty) — physics.stackexchange.com
9. [Whats the difference between an uncertainty and an error?](https://www.reddit.com/r/AskPhysics/comments/sprnil/whats_the_difference_between_an_uncertainty_and) — reddit.com
10. [Error and uncertainty | FIDUCEO](https://www.fiduceo.eu/tutorial/error-and-uncertainty) — fiduceo.eu
11. [What is the Combined Uncertainty](https://www.isobudgets.com/faq/what-is-combined-uncertainty) — isobudgets.com
12. [JCGM 100:2008 Evaluation of measurement data](https://ncc.nesdis.noaa.gov/documents/documentation/JCGM_100_2008_E.pdf) — ncc.nesdis.noaa.gov
13. [Measurement Uncertainty Budget Calculator — GUM / JCGM 100:2008 | SieveCalc.Pro](https://sievecalc.pro/tools/gum-uncertainty-budget) — sievecalc.pro
14. [JCGM 100:2008 Made Clear – A Clause-by-Clause Guide ...](https://www.linkedin.com/pulse/jcgm-1002008-made-clear-clause-by-clause-guide-anil-s-rawat-wvntf) — linkedin.com
