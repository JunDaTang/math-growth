---
type: query
title: "Research: 《分析概率论》(Théorie analytique des probabilités, 1812)"
created: 2026-09-28
origin: deep-research
tags: [research]
---

# Research: 《分析概率论》(Théorie analytique des probabilités, 1812)

# 《分析概率论》(Théorie analytique des probabilités, 1812)

## 概述

《分析概率论》（法文原名 *Théorie analytique des probabilités*）是法国数学家皮埃尔-西蒙·拉普拉斯（Pierre-Simon Laplace，1749–1827）于 1812 年在巴黎出版的专著 [2][5]。该书将 1713 年雅各布·伯努利（Jakob Bernoulli）《推测术》（*Ars Conjectandi*）以来直至拉普拉斯本人近四十年研究的主要概率论成果，整合进统一的数学框架之中，并确立了此后一个多世纪主导该学科的解析方法——母函数（generating functions）、特征函数（characteristic functions）、渐近逼近、最小二乘法以及[[中心极限定理|中心极限定理]] [5]。

该书被视为拉普拉斯晚年学术生涯的基石性成果，也是把数学确立为对"人类与自然事件"进行定量研究的工具的关键著作 [5]。中文学界对该书译名不一，常见有《分析概率论》《概率的分析理论》以及《概率论——概率之解析理论》等 [12][13][14][15]。

## 版本与出版信息

- **出版者与年份**：1812 年由巴黎的 Veuve Courcier（"Courcier 寡妇"）出版，出版者全称在不同书目中记作 "M.me V. Courcier, Imprimeur-Libraire pour la Mathématiques, quai des Augustins. Paris" [3][5]。部分馆藏记录另将 1820 年版本列为独立条目，署"Courcier, Ve. (1820)" [1]。
- **带补充卷的版本**：现存版本常以"附四篇补充（With the four supplements）"形式出现，时间跨度记为 1812–25 年，出版者 Paris: Veuve Courcier [4]。这说明该书并非一次性定稿，而是以初版加若干补充卷的形式持续扩充。
- **初版序言的处理**：初版所附、由拉普拉斯本人撰写的序言，在第二、第三版中被删除，改由《Essai philosophique》（《概率的哲学导论》）取代 [5]。因此不同版本在"导论性文字"上存在实质差异，引用时须注明版本。

## 内容纲领

据初版序言所述，拉普拉斯的写作旨趣在于：确定"成因与结果"的概率，这些概率体现在大量重复发生的事件之中，并研究这些概率依事件重复次数而趋近某一极限的规律 [5]。这一表述同时涵盖了两条主线：

1. **由因推果（正问题）**：在已知模型/成因的前提下计算结果的概率；
2. **由果溯因（[[概率p的置信区间|逆概率]]问题）**：由观测结果反推成因的概率。

## 主要贡献

### 古典概率定义与学科综合

中文文献普遍指出，拉普拉斯在 1812 年此书中"首先明确地对概率作了古典的定义"，把分析方法引入概率论，系统地总结了 18 世纪概率论的研究成果 [12][13]。据百度百科条目，该书是在拉普拉斯 1810 年至 1811 年间撰写的多篇论文基础上整合而成，系统总结了 18 世纪概率论研究成果并引入分析方法 [15]。

### 中心极限定理

该书包含拉普拉斯对[[中心极限定理|中心极限定理]]最为一般的陈述：当独立观测的数目增大时，其均值的分布趋向高斯形式，而与单个观测的分布无关；并且"均值以给定概率落入的区间界限，随观测数目的增大而彼此靠拢" [5]。拉普拉斯以出生记录作为经验材料来演示该定理——取自巴黎、伦敦、那不勒斯登记册的男女出生比例，为后续分析提供了先验概率的经验数值 [5]。

关于该定理的历史归属，几处来源可相互印证：

- 莫弗（De Moivre）的相关发现"远远超前于其时代"，在近百年内几乎被遗忘，直到拉普拉斯在其中巨著《分析概率论》（1812）中将其重新发掘 [6]。这也解释了为何相关结果被称为[[棣莫弗-拉普拉斯局部极限定理|棣莫弗-拉普拉斯定理]] [14][8]。
- 拉普拉斯实际上在 1810 年就已发现该基本定理的要点 [7]。
- 关于严格化：有评论认为"该极限定理的真正发现者应归拉普拉斯；其严格证明可能最早由切比雪夫（Tschebyscheff）给出，而最精确的表述见于[[李雅普诺夫|李雅普诺夫]]（Liapounoff）的文章" [6]。现代形式的精确陈述则迟至 1920 年代才出现 [6]。
- "中心"（central）这一命名由 Pólya 给出，用以强调该定理在概率论中的核心地位 [6]。

拉普拉斯的证明使用了母函数方法，并对极值作了某种形式的分析 [9][5]。

### 逆概率与统计推断框架

有来源指出，拉普拉斯不仅"打开了逆概率问题"，还把它用作发现中心极限定理的"强力催化剂" [10]。更晚近的回顾性分析认为，拉普拉斯的工作"超越了简单的逆概率，形成了一个系统的统计推断框架" [11]。这为后来[[数理统计|数理统计]]中的[[假设检验与残概率|假设检验]]、[[概率p的置信区间|置信区间]]等思想提供了早期原型。

### 解析方法工具箱

该书奠定了此后长期主导学科的解析方法，具体包括：母函数、特征函数、渐近逼近、[[最小二乘法|最小二乘法]]以及中心极限定理 [5]。这些方法在后续文献中反复出现——例如[[数学指南-实用数学手册|《数学指南——实用数学手册》]]中关于[[极限定理|极限定理]]、[[斯特林公式|斯特林公式]]与[[泊松逼近定理|泊松逼近]]的现代处理，均可视为这一解析传统的延续（参见 [[10-数学指南实用数学手册--8-624-极限定理--73k7xm]]）。

### 应用算例

除男女出生比例外，拉普拉斯在书中还计算了某一"周日模式（diurnal pattern）"归因于规则性成因（太阳的作用）而非偶然的概率，并确定了其平均幅度 [5]。

## 历史地位与影响

- **统一框架**：该书把自 1713 年《推测术》以来分散的概率论结果"编纂进一个统一的数学框架" [5]。
- **学科转向**：它使概率论从早期以组合计数为主的阶段，转向以分析工具为核心的新阶段，中文文献称其"使概率论发展到一个新阶段" [13]。
- **统计推断的源头**：书中确立的方法支撑了此后一个多世纪的概率论与数理统计（见 [2]、[11]）。

## 与既有 wiki 条目的关联

- [[中心极限定理]]、[[极限定理]]：该书是这些定理在现代文献中被追溯的源头 [5][6][7]。
- [[棣莫弗-拉普拉斯局部极限定理]]、[[棣莫弗-拉普拉斯全面极限定理]]：因拉普拉斯的重新发掘而得名 [6][14]。
- [[切比雪夫]]、[[李雅普诺夫]]：中心极限定理严格化的后续贡献者 [6]。
- [[最小二乘法]]：拉普拉斯方法工具箱的核心组成部分 [5]。
- [[泊松分布]]、[[泊松逼近定理]]、[[伯努利模型]]、[[二项分布]]：属于该书所综合的 18 世纪概率论成果谱系。
- [[概率p的置信区间]]、[[假设检验与残概率]]、[[数理统计]]：可追溯到该书开创的逆概率/推断思路 [10][11]。

## 矛盾与空白

1. **出版年份的多重记载**：来源 [2][3][5] 明确记为 1812 年首版，而 [1]（archive.org）所列馆藏为 1820 年，[4] 则记为 1812–25 年（含四篇补充）。这些并不必然冲突（初版、后续版本与补充卷之区分），但需在引用时厘清所指版本。
2. **序言差异**：初版序言与第二、三版以《Essai philosophique》充当导论的做法不同 [5]，关于"该书纲领"的引述应标注版本来源。
3. **定理归属的表述张力**：[6] 一方面承认拉普拉斯"重新发掘"莫弗的成果，另一方面又引证"真正发现者应归拉普拉斯"的说法；这与中文文献强调"棣莫弗-拉普拉斯定理"并置命名的做法 [14] 存在叙事侧重上的差异。是否将 1810 年的发现与 1812 年成书视为同一贡献，来源 [7] 与 [6] 亦有不同强调。
4. **补充卷内容缺失**：来源 [4] 提及"四篇补充"，但现有材料未列出各补充卷的具体内容与年份，形成明显空白。
5. **严格化的时间线**：来源 [6] 称现代形式的精确陈述迟至 1920 年代，而中文来源多止于"古典定义/分析方法"的概括 [12][13][15]，两端之间的证明史（切比雪夫—李雅普诺夫脉络）在本主题的来源中着墨甚少。

## 建议补充的来源

- 拉普拉斯本人 1810、1811 年发表于 *Mémoires de l'Académie des Sciences* 的相关论文，以核实 [15] 所称"1810–1811 年多篇论文"整合之说。
- 该书第二、第三版（含《Essai philosophique》）及其四篇补充卷的完整书目与内容目录。
- 关于 1812 年版流传与存世情况的版本学研究（现有来源 [5] 已提示其流传稀有性，但缺乏系统版本谱系）。
- Anders Hald 等关于 18–19 世纪概率论与统计史的专著，用于交叉验证中心极限定理归属的叙述 [6][7]。
- 关于拉普拉斯逆概率（inverse probability）与贝叶斯方法的对比研究，以厘清 [11] 所称"系统统计推断框架"的具体边界。

## References

1. [Théorie analytique des probabilités : Laplace, Pierre Simon, marquis de ...](https://archive.org/details/theorieanaldepro00laplrich) — archive.org
2. [P.S. Laplace, Théorie analytique des probabilités, first edition (1812)](https://www.sciencedirect.com/science/chapter/edited-volume/pii/B9780444508713501054) — sciencedirect.com
3. [Le Comte, L.M. (1812) Théorie Analytique des Probabilités, M.me ...](https://www.scirp.org/reference/referencespapers?referenceid=1628171) — scirp.org
4. [Théorie analytique des probabilités, Pierre-Simon Laplace, 1812–25](https://onlineonly.christies.com/s/fine-printed-books-manuscripts-science/theorie-analytique-des-probabilites-74/325345) — onlineonly.christies.com
5. [Théorie Analytique des Probabilités. Paris: Courcier, 1812. With](https://www.sophiararebooks.com/pages/books/6347/pierre-simon-laplace-marquis-de/theorie-analytique-des-probabilites-paris-courcier-1812-with-supplement-a-la-theorie-analytique) — sophiararebooks.com
6. [Central limit theorem - Wikipedia](https://en.wikipedia.org/wiki/Central_limit_theorem) — en.wikipedia.org
7. [[PDF] A History of the Central Limit Theorem](https://ndl.ethernet.edu.et/bitstream/123456789/19811/1/19.pdf) — ndl.ethernet.edu.et
8. [Rigorous, real analysis, proof of De Moivre–Laplace theorem](https://math.stackexchange.com/questions/2091338/rigorous-real-analysis-proof-of-de-moivre-laplace-theorem) — math.stackexchange.com
9. [[PDF] Studying “moments” of the Central Limit theorem](https://scholarworks.umt.edu/cgi/viewcontent.cgi?article=1388&context=tme) — scholarworks.umt.edu
10. [Pierre-Simon Laplace, Inverse Probability, and the Central Limit ...](https://medium.com/data-science/pierre-simon-laplace-inverse-probability-and-the-central-limit-theorem-d52bec2e0dba) — medium.com
11. [解读《概率分析理论》 - alphaXiv](https://www.alphaxiv.org/zh/abs/1203.6249) — alphaxiv.org
12. [概率论的起源、发展、应用 - 统计之都](https://cosx.org/2008/11/probability-theory-origin-development-application/) — cosx.org
13. [概率论与数理统计发展简史 - 知乎专栏](https://zhuanlan.zhihu.com/p/13963316094) — zhuanlan.zhihu.com
14. [概率論史- 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/%E6%A6%82%E7%8E%87%E8%AE%BA%E5%8F%B2) — zh.wikipedia.org
15. [概率的分析理论_百度百科](https://baike.baidu.com/item/%E6%A6%82%E7%8E%87%E7%9A%84%E5%88%86%E6%9E%90%E7%90%86%E8%AE%BA/19137689) — baike.baidu.com

## Related
- [[queries/research-泊松siméon-denis-poisson-2026-09-27-162558-research-77]]
- [[queries/research-拉普拉斯女婴频率数据与沃尔夫投针实验的历史来源核实-2026-09-27-161332-research-50]]
