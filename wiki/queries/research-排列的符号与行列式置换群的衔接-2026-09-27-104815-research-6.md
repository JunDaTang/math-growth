---
type: query
title: "Research: 排列的符号与行列式/置换群的衔接"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 排列的符号与行列式/置换群的衔接

# 排列的符号与行列式／置换群的衔接

## 概述

本页综合所收集的资料，梳理三条相互交织的线索：**排列（置换）的符号**、**行列式的莱布尼茨展开**，以及**置换群／对称群的理论框架**。这三条线索表面分属组合学、多重线性代数与群论，实则共享同一个核心对象——对称群 $S_n$ 及其符号同态。资料 [10]–[14] 直接给出了"行列式随行（列）置换乘以该置换的符号"这一关键关系；[2]、[8]、[9] 提供了排列、对换与符号的教学式处理；[5]–[7] 则展示了置换群向群论一般理论及其应用的延伸。需要指出，[4]（法國電影新浪潮）与本主题无实质关联，属于检索噪声，下文不再引用。

## 排列、置换与对称群

排列（全排列）与置换在结构上是一回事：一个全排列确定集合 $M$ 的一个双射变换，不同的排列确定不同的变换 [8]。这一"把排列等同于双射"的视角，正是从具体的置换群走向一般抽象群的关键一步——[8] 明确指出，正因如此，置换群的研究被推进到更一般的抽象群研究之上。

[9] 的笔记以 $S_n$ 记 $n$ 元对称群，并把偶置换的全体定义为**交错群** $A_n$；同时引述 **Cayley 定理**，即任意群 $G$ 同构于 $G$ 上对称群的一个子群（原文为"所有群 G 同构于在 G 上的对称群的子群"）。[14] 则从最小的例子入手：$S_1$ 只有一个置换，$S_2$ 有两个置换；其中恒等置换 $\mathrm{id}$ 的符号为 $1$，另一个置换 $\sigma$ 的符号为 $-1$。

## 排列的符号（奇偶性）与对换

关于符号的定义，资料存在两种常见表述：

- **符号函数定义**：[9] 以符号函数的取值定义——符号为 $1$ 者称**偶置换（even）**，符号为 $-1$ 者称**奇置换（odd）**，$S_n$ 中所有偶置换构成交错群 $A_n$。
- **对换定义**：[2] 在引出 $n$ 阶行列式定义的过程中，专门讨论**对换**的概念及其与排列的关系；[13] 亦指出莱布尼茨使用了现代意义上的"换位（transposition）"概念来处理符号规则。

[13] 特别强调，无论采用何种等价表述，"符号规则是等价的（The sign rules are equivalent）"，因为一个置换的奇偶性是其内在属性，并不依赖于分解方式。这一观察在教学中常被当作引理，但各来源均未给出完整的证明（见下文"空白"一节）。

## 从排列符号到行列式：莱布尼茨公式

行列式的现代定义直接建立在排列符号之上。教材 [2] 的思路是先根据二阶、三阶行列式的规律"引出 $n$ 阶行列式的定义"，为此需要先讨论对换与排列——这正说明符号概念是行列式定义的必要前置。[12] 则把这一构造形式化：行列式可写成对对称群 $S_n$ 上的**双重排列展开（double permutation expansion）**，它"自然地推广了方阵行列式的经典莱布尼茨公式"，随后作者专门分析其符号项。这说明符号不仅在经典行列式中出现，在推广到立方矩阵等对象时仍是定义的核心部件。

行列式的另一侧叙述是**性质式的**：[2] 提到"行列式的某一行（列）的所有元素的公因子可以提到行列式符号……"；而更直接对应本主题的，是 [10]、[11] 所给的定理：

> 行列式的值改变符号。若把 $A$ 的行 $1,2,\dots,n$（列）排成序列 $k_1,k_2,\dots,k_n$，则行列式乘以该排列的符号。

这条命题把"交换行列变号"这一行列式公理与"排列的符号"精确对应起来：对换一次相当于乘 $-1$，任意置换的累积效果即其符号 $(-1)^{N(\sigma)}$。

在已有的 wiki 体系中，这一关系还以另外两条路径被记录：[[例2三重外积等于行列式]] 表明三重外积等于行列式，[[行列式与反称n线性型关系]] 则把行列式刻画为反称 $n$ 线性型。这两条路径与排列符号路径互为印证——[[反称性]] 与 [[反称多线性型]] 中的换序变号，本质上是符号同态在多重线性框架下的表现。相关的更广背景可参见 [[多线性代数]]、[[外积]] 与 [[线性代数]]。

## 置换群与群论的一般框架

置换群不仅是行列式的工具，也是群论的起点与归宿：

- **结构方向**：[6] 介绍有限群的结构定理（如 $p$ 群的结构定理）及有限群在几何、晶体学、量子力学、化学反应对称性等领域的应用；[5] 从物理学的角度处理对称群、置换群、杨算符以及各类矩阵群的不可约张量基计算，并指出若新基只是改变原有基的排列次序，则相似变换也只改变矩阵行（列）的排列次序——这与列/行置换的行列式变号规则形成呼应。
- **应用方向**：[7] 讨论交叉立方体中一类保维自同构，证明这些自同构在合成运算下构成群。这是置换群/自同构群在网络与图论中的一个具体应用实例。
- **抽象化方向**：如前述 [8] 所述，由置换群走向一般抽象群。

## 历史脉络：莱布尼茨与消元法

[1] 与 [13] 都把行列式的概念起源追溯到莱布尼茨。[1] 称其"首次引入行列式概念，创立符号逻辑学基本概念"，并提到莱布尼茨的消元法研究；[13] 则以"莱布尼茨发明了行列式理论（that Leibniz invented determinant theory）"的转述形式讨论其"变差（variation）"概念，并强调他使用了现代意义上的换位概念。[10] 以"莱布尼茨的消元与行列式理论"为题，正是把符号规则放在其消元算法传统中考察。此外，[3] 提到用 $b$ 替代第 $i$ 列得到行列式的做法，即 **Cramer 法则**（克莱姆法则）形式的应用，可视为行列式—线性方程组求解这一历史动机的延续。

## 矛盾与空白

1. **来源重复**：[10] 与 [11] 的核心段落几乎逐字相同（"the value of the determinant changes its sign … multiplied by the sign of this permutation"）。二者高度疑为同一文本的不同收录载体，引用时应视作单一证据，而非两项独立佐证。
2. **定义的多样性未整合**：符号函数定义 [9]、对换定义 [2][13]、以及由行列式性质反推符号 [10][11]，三种进路在本批资料中并未被明确证明等价，仅有 [13] 的一句断言。
3. **关键定理缺失**：本批资料未给出符号同态 $\operatorname{sgn}: S_n \to \{\pm 1\}$ 的核恰为 $A_n$、$A_n \triangleleft S_n$ 且 $[S_n:A_n]=2$ 的证明；亦未给出**置换矩阵** $P_\sigma$ 满足 $\det P_\sigma = \operatorname{sgn}(\sigma)$ 这一衔接行列式与置换群的桥梁命题。
4. **史料争议**：[1] 与 [13] 均称莱布尼茨"首次引入/发明"行列式，但 [13] 的表述是转述（"that Leibniz invented…"），其原始归属与优先权仍有讨论空间。
5. **无关注释**：[4] 与本主题无关，建议在来源整理中剔除或标注。
6. **wiki 覆盖空白**：现有索引中尚无"置换群""对称群 $S_n$""交错群 $A_n$""排列的符号""莱布尼茨公式""Cayley 定理"等条目，本主题的核心概念大多需新建页面。

## 建议补充的来源

- 关于**置换矩阵**与 $\det P_\sigma = \operatorname{sgn}\sigma$ 的线性代数教材章节，用于补足上文的桥梁命题。
- **Cayley 定理**的原始文献与标准证明（可与 [9] 的引述对照）。
- 关于符号同态 $\operatorname{sgn}$ 与交错群 $A_n$ 的群论教材，以补足正规子群与指标 $2$ 的论证。
- 行列式历史的专门研究（如 Weierstrass、Jacobi、MacMahon 的贡献），以校正 [1][13] 关于莱布尼茨优先权的叙述。
- 对称群表示论与**杨算符**的物理教材（[5] 可作入门），用以连接置换群与不可约张量基。
- 与 [[反称多线性型]]、[[行列式与反称n线性型关系]] 直接对应的教材章节，以便在本页与既有"外积—反称性"路线之间建立双向链接。

## References

1. [莱布尼茨部分数学手稿探赜](https://html.rhhz.net/XBDXXBZRKXB/file-2018-10-16-15.html) — html.rhhz.net
2. [线性代数](https://books.google.com/books?hl=en&lr=&id=yQ6VEAAAQBAJ&oi=fnd&pg=PA1&dq=%E6%8E%92%E5%88%97%E7%9A%84%E7%AC%A6%E5%8F%B7+sgn+%E8%A1%8C%E5%88%97%E5%BC%8F+%E5%AE%9A%E4%B9%89+%E8%8E%B1%E5%B8%83%E5%B0%BC%E8%8C%A8%E5%85%AC%E5%BC%8F&ots=8F_Pc1tQwz&sig=TidHtPesn3vOjxMpQusSDfqXMp4) — books.google.com
3. [科学和工程计算基础](https://books.google.com/books?hl=en&lr=&id=qtyGmvPT7gEC&oi=fnd&pg=PR3&dq=%E6%8E%92%E5%88%97%E7%9A%84%E7%AC%A6%E5%8F%B7+sgn+%E8%A1%8C%E5%88%97%E5%BC%8F+%E5%AE%9A%E4%B9%89+%E8%8E%B1%E5%B8%83%E5%B0%BC%E8%8C%A8%E5%85%AC%E5%BC%8F&ots=jqufPtOxM8&sig=ROf5IDPLpLIL3FzzTHW_JpXikKM) — books.google.com
4. [法國電影新浪潮](https://books.google.com/books?hl=en&lr=&id=Ytr0DwAAQBAJ&oi=fnd&pg=PA1917&dq=%E6%8E%92%E5%88%97%E7%9A%84%E7%AC%A6%E5%8F%B7+sgn+%E8%A1%8C%E5%88%97%E5%BC%8F+%E5%AE%9A%E4%B9%89+%E8%8E%B1%E5%B8%83%E5%B0%BC%E8%8C%A8%E5%85%AC%E5%BC%8F&ots=p2q23BC86m&sig=6FNBwabE245GkttOA-pRh_htgLo) — books.google.com
5. [物理学中的群论](http://www.ecsponline.com/yz/BE1D35EF7D37641079C3677D2794FE685000.pdf) — ecsponline.com
6. [有限群的基本理论与应用](https://pdf.hanspub.org/PM20231200000_34898594.pdf) — pdf.hanspub.org
7. [关于交叉立方体中一类保维自同构群的讨论](https://xbzrb.gdut.edu.cn/article/doi/10.3969/j.issn.1007-7162.2013.03.018) — xbzrb.gdut.edu.cn
8. [近世代数](http://idl.hbdlib.cn/book/00000000000000/pdfbook/o/o01/index0069.pdf) — idl.hbdlib.cn
9. [对称群笔记](https://whzecomjm.com/p/2020/07/symmetric-groups-notes/Symmetric-Groups.pdf) — whzecomjm.com
10. [Leibniz's theory of elimination and determinants](https://link.springer.com/chapter/10.1007/978-4-431-54273-5_17) — link.springer.com
11. [Determinant theory, symmetric functions, and dyadic](https://books.google.com/books?hl=en&lr=&id=XrRwDwAAQBAJ&oi=fnd&pg=PA225&dq=determinant+Leibniz+formula+sign+of+permutation&ots=8vYcuMNTNT&sig=LnLXfreh1uzLNeBq8FniWmOrxmI) — books.google.com
12. [A PERMUTATION-BASED DETERMINANT FOR CUBIC MATRICES AND ITS LAPLACE-TYPE EXPANSIONS](https://www.researchgate.net/profile/Orgest-Zaka-2/publication/405951630_A_PERMUTATION-BASED_DETERMINANT_FOR_CUBIC_MATRICES_AND_ITS_LAPLACE-TYPE_EXPANSIONS/links/6a214f39ab2754591108d32f/A-PERMUTATION-BASED-DETERMINANT-FOR-CUBIC-MATRICES-AND-ITS-LAPLACE-TYPE-EXPANSIONS.pdf) — researchgate.net
13. [The notion of variation in Leibniz](https://link.springer.com/chapter/10.1007/978-94-007-2627-7_14) — link.springer.com
14. [Permutations and the Determinant](https://www.math.ucdavis.edu/~anne/WQ2007/mat67-Lm-Determinant.pdf) — math.ucdavis.edu

## Related
- [[queries/research-是否将-211-组合学与-212-行列式的排列工具合并交叉引用-2026-09-27-104820-research-8]]
- [[queries/research-变形彩票问题-2026-09-27-104649-research-4]]
