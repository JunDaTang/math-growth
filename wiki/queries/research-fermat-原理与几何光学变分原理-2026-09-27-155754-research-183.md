---
type: query
title: "Research: Fermat 原理与几何光学变分原理"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: Fermat 原理与几何光学变分原理

# Fermat 原理与几何光学变分原理

Fermat 原理（Fermat's principle，又称「最短时间原理」，英语亦称 Principle of Least Time）是几何光学的核心变分原理，也是连接光学、经典力学与近代量子力学的关键思想节点。它以「路径取极值」的方式概括了光的传播规律，可用来统一推导反射定律、折射定律（Snell 定律）等一系列几何光学结论。中文语境中常被称为费马原理，本页将「Fermat 原理」「费马原理」「最短时间原理」视为同一对象的异名表述 [11][12][15]。

## 历史背景

费马原理最早由法国科学家皮埃尔·德·费马（Pierre de Fermat）于 1662 年提出 [11][12][15]。其最初形式被表述为「最短时间原理」：光从一点传播到另一点时，所选路径对应的时间最短 [3][4]。在费马所处的时代，这一思想为折射定律提供了不同于波动说的解释路径；由于折射时光速在不同介质中不同，最短时间原理实际上隐含了「介质中光速与折射率成反比」的判断，这一点后来成为区分光的微粒说与波动说的历史线索之一。

在中文的科普与教材传统中，费马原理的表述通常已经过修正：光传播的路径是**光程取极值**的路径，而该极值可能是极大值、极小值，甚至是函数的拐点 [11][12][15]。这一修正反映了人们对该原理适用范围认识的深化。

## 原理的精确表述：驻定而非「最短」

关于费马原理最常见的误解是把它理解为「光总是走最短时间的路径」。更准确的表述是：**光所走的路径是使传播时间在路径的微小扰动下保持驻定（stationary）的路径** [2]。也就是说，沿实际光线的时间相对于路径的一阶变分为零，因此该极值既可能是极小值，也可能是极大值或鞍点，具体取决于光学系统 [11][12][13][14]。

Wikipedia 词条在其注解中专门讨论了「驻定时间」与「最小时间」的区别 [1]：若从较早的波前整体来计量时间，则该时间处处恰为 Δt，谈论「驻定」或「最小」时间便失去意义。只有当次级波前比初级波前更凸（如常见情形）时，「驻定时间」才恰好是**最小**时间。然而这一前提并非总成立：例如当初级波前在某个次级波前的范围内会聚成一个焦点并重新发散时，次级波前将从外侧而非内侧与较晚的初级波前相切。为容纳这类复杂性，必须满足于使用「驻定时间」而非「最小时间」的说法 [1]。这一讨论引用了 Born & Wolf《光学原理》中关于「正则邻域」（regular neighbourhood）的论述（见 [1] 所引 pp.136–7）。

physixfan、科学空间等中文来源同样强调了这一点：过空间中两定点的光，实际路径总是光程最短、最长或恒定值的路径 [13][14]。kexue.fm 给出了具体例证：凸透镜成像即对应光程为**恒定值**的情形，而非极小值 [14]。

## 光程与折射率

费马原理的量化语言是**光程**（optical path）。在折射率为 n 的均匀介质中，光程定义为折射率与几何路程的乘积；对折射率随位置变化的介质，则取积分

$$L = \int n\, ds,$$

而在由若干均匀介质段组成的路径上，光程为各段「折射率 × 路程」之和 [13]。费马原理可等价地表述为：实际光路使光程 L 取极值（在均匀介质中，因光速恒定，光程极值等价于时间极值）。这一等价使原理在处理分层介质、渐变折射率介质等问题时尤为方便。

## 从 Fermat 原理导出反射与折射定律

费马原理的重要价值在于：它可以把几何光学的基本定律作为变分问题的解统一导出。

- **反射定律**：光在界面反射时，入射角等于反射角。该结论可视为在两个定点之间、约束于点经过镜面的路径集合上求时间极值的结果——几何上等价于把其中一点对镜面作镜像反射后连接两点的直线。Huygens 原理同样可以用来证明反射定律 [6]。
- **折射定律（Snell 定律）**：光在两介质界面折射时，入射角与折射角的正弦之比等于两介质折射率之比。其推导方式是对跨越界面的路径参数求光程的一阶变分为零，由此得到 $\sin\theta_1 / \sin\theta_2 = v_1 / v_2 = n_2 / n_1$ 类的关系 [3]。多份资料以「由费马原理推导 Snell 定律」为教学主题，说明这是该原理最典型、最具说服力的应用 [3]。

## 与 Huygens 原理的关系

Fermat 原理与 Huygens 原理是几何光学的两大经典支柱，二者在描述光的传播上互为补充：Fermat 原理以「路径」为出发点，给出整体性（积分型）的极值条件；Huygens 原理以「波前」为出发点，把每一点视为次级子波源，其包络（envelop）构成新的波前 [6][7][9]。用 Huygens 原理可以证明反射定律 [6]，而用 Fermat 原理可以导出折射定律；在适当的凸性条件下，两者可以相互印证。前述 [1] 对「驻定/最小」的讨论正是借助波前的几何关系（次级波前与初级波前的相切方式）来澄清 Fermat 原理的适用范围，说明两大原理在深层上是相通的。

需要注意的是，多份来源把「波传播方向垂直于波前」作为 Huygens 作图的基础常识 [8][9][10]，这是由光的横波性质所决定的方向约定，与 Fermat 原理中的光程极值并不矛盾，而是描述同一现象的不同侧面。

## 与变分原理、最小作用量原理及量子力学的联系

费马原理在方法论上属于**变分原理**：它用「某积分量取极值/驻定」来刻画物理过程的实际路径。这一结构在物理学中被反复借用——力学中的最小作用量原理（Hamilton 原理）在数学形式上与费马原理高度相似，这也是历史上从光学类比走向分析力学的关键线索之一。

在近代物理中，该思想进一步延伸到量子领域。[[费恩曼]]（R. P. Feynman）发展的路径积分（即 [[费恩曼积分]]）可以看作费马原理的量子推广：经典光学的「取极值路径」在量子情形下被扩展为对所有路径的加权求和，其中极值路径在经典极限下重新浮现。这条思想链条把 [[费马]] 提出的光学原理，与 [[费恩曼积分]] 所代表的量子力学表述方式联系了起来，并与本维基所收录的《数学指南——实用数学手册》6.4 节中关于随机过程、[[维纳积分]]、[[量子过程的随机性]] 等议题构成更大的知识网络。

## 争议、缺口与注意事项

1. **「最短」与「驻定」的表述差异**：大众化资料（如 [3][4] 及众多教学视频）倾向于直接说「最短时间」，而更严谨的文献（[1][2][13][14]）强调应为「驻定时间」。这并非根本性的理论冲突，而是适用范围与严格性的差异；在撰写或讲授时宜明确区分 [2]。
2. **极值类型的判据**：现有资料普遍指出极值可以是极小、极大或拐点 [11][12][13][14]，但对「何时为极大、何时为极小、何时为恒定值」的判据，多停留在举例（如凸透镜成像为恒定值 [14]），缺少系统性的成立条件论述；[1] 中关于次级波前凸性、焦点的讨论提供了部分线索，可参考 Born & Wolf 的「正则邻域」概念补足。
3. **光程定义的严格性**：中文来源给出了「折射率 × 路程」的简洁定义 [13]，但对折射率连续变化介质的积分定义及其与时间表述的等价性，来源中未展开证明，需补充。
4. **历史细节**：费马提出该原理的年份在中文来源中一致记为 1662 年 [11][12][15]，但关于其原始表述是「最短时间」还是「极值」的史料细节，本批来源未给出，宜进一步查证。

## 建议补充的来源

- Born & Wolf,《Principles of Optics》中关于「regular neighbourhood」与驻定/最小时间区别的章节（对应 [1] 所引 pp.136–7）。
- 费马 1662 年原始论述的英译本或权威科学史文献，用以核实「最短时间」到「极值」的表述演变。
- 最小作用量原理与费马原理之间形式类比的标准教材论述（分析力学方向）。
- Feynman 关于路径积分与经典极限的原始论文（如 Rev. Mod. Phys. 1948），用于补全从费马原理到 [[费恩曼积分]] 的推导细节。

## 关联条目

- [[费马]] —— 费马原理的提出者
- [[费恩曼]] —— 路径积分（费恩曼积分）的提出者
- [[费恩曼积分]] —— 费马原理在量子力学层面的推广
- [[维纳积分]]、[[量子过程的随机性]] —— 与「对路径求和」思想相关的数学结构

## References

1. [Fermat's principle - Wikipedia](https://en.wikipedia.org/wiki/Fermat%27s_principle) — en.wikipedia.org
2. [How does Fermat's principle make light choose a straight path over a ...](https://physics.stackexchange.com/questions/567920/how-does-fermats-principle-make-light-choose-a-straight-path-over-a-short-path) — physics.stackexchange.com
3. [Fermat's Principle to Snell's Law (Derivation) - YouTube](https://www.youtube.com/watch?v=3Etj75qzGg0) — youtube.com
4. [3.Fermat's Principle of Least Time - Galileo and Einstein](https://galileoandeinstein.phys.virginia.edu/7010/CM_03_FermatLeastTime.html) — galileoandeinstein.phys.virginia.edu
6. [Reflection laws proof using Huygen's principle | Class 12 - YouTube](https://www.youtube.com/watch?v=N3levs4TzTA) — youtube.com
7. [Huygens's Principle: Diffraction | Physics II - Lumen Learning](https://courses.lumenlearning.com/atd-austincc-physics2/chapter/27-2-huygenss-principle-diffraction/) — courses.lumenlearning.com
8. [Huygens's Principle: Diffraction – Introductory Physics for the Health ...](https://openbooks.lib.msu.edu/collegephysics2/chapter/huygenss-principle-diffraction-2/) — openbooks.lib.msu.edu
9. [1.7: Huygens's Principle - Physics LibreTexts](https://phys.libretexts.org/Bookshelves/University_Physics/University_Physics_(OpenStax)/University_Physics_III_-_Optics_and_Modern_Physics_(OpenStax)/01%3A_The_Nature_of_Light/1.07%3A_Huygenss_Principle) — phys.libretexts.org
10. [Why is the direction of a light wave perpendicular to its wavefront?](https://www.quora.com/Why-is-the-direction-of-a-light-wave-perpendicular-to-its-wavefront) — quora.com
11. [光学原理回顾：费马原理 - 知乎专栏](https://zhuanlan.zhihu.com/p/339379757) — zhuanlan.zhihu.com
12. [费马原理- 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/%E8%B2%BB%E9%A6%AC%E5%8E%9F%E7%90%86) — zh.wikipedia.org
13. [最小作用量原理与物理之美2——费马原理 - physixfan](https://www.physixfan.com/zuixiaozuoyongliangyuanliyuwulizhimei3-feimayuanli/) — physixfan.com
14. [《自然极值》系列——2.费马原理 - 科学空间|Scientific Spaces](https://kexue.fm/archives/1068) — kexue.fm
15. [费马原理_百度百科](https://baike.baidu.com/item/%E8%B4%B9%E9%A9%AC%E5%8E%9F%E7%90%86/1202408) — baike.baidu.com
