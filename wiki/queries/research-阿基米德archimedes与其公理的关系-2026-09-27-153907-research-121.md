---
type: query
title: "Research: 阿基米德（Archimedes）与其公理的关系"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 阿基米德（Archimedes）与其公理的关系

# 阿基米德（Archimedes）与其公理的关系

## 概述

「阿基米德公理」（Archimedes' axiom），又称「连续性公理」（continuity axiom）或「阿基米德引理」（Archimedes' lemma），是数学分析、实数理论与几何基础中的一个基本命题 [1][5]。它刻画了这样一个直观事实：任意两个同类的量，只要其一非零，就可以通过不断累加较小的量来超过较大的量——换言之，不存在「无穷小」或「无穷大」的元素 [14]。

一个值得注意的是：这条以阿基米德命名的公理，其最早的系统表述实际上见于欧多克索斯（Eudoxus）的著作，早于阿基米德本人 [1][5][7]。阿基米德本人在手稿中坦承了这一点，但遵从传统，后世仍以他的名字来称呼这条性质 [7]。因此，「阿基米德与其公理的关系」包含两个层面：一是阿基米德作为公理 **命名者** 的历史地位，二是他在 **传承与使用** 欧多克索斯成果时所扮演的角色。

## 阿基米德其人

阿基米德（希腊语：´Αρχιμήδης；约前 287 年—前 212 年）是希腊化时代的数学家、物理学家、发明家、工程师与天文学家 [6]。他出生于西西里岛的叙拉古（Syracuse），据说曾在亚历山大里亚（Alexandria）求学 [6]。他被后世誉为「数学之神」 [8]，其父本身即是天文学家与数学家 [9]。

阿基米德的贡献横跨数学与物理两大领域：他创立了「浮体理论」（即著名的阿基米德原理）与「杠杆原理」 [9]；在数学上，他研究计算几何图形的面积与体积，并给出了圆周率的估计 [10]。这些工作共同奠定了他作为古代最伟大科学家之一的地位。

据传，阿基米德原本有一部传记，作者是他的朋友赫拉克利德（Heraclides）——此人与公元前 6 世纪的哲学家赫拉克利特（Heracleitus）并非同一人，也非同处一个时代 [8]。

## 阿基米德公理的内容与表述

不同来源给出了等价但形式各异的表述：

- **现代分析表述**：给定两个量 $a$ 与 $b$，且 $a < b$，则存在一个自然数 $m \in \mathbb{N}$，使得 $ma > b$ [4]。这正是「阿基米德性质」（Archimedean property）的典型形式，即实数系中不存在无穷大或无穷小元素 [14]。
- **古典几何表述**：给定两个有比（ratio）的量，可以找到其中一个的某个倍数使之超过另一个 [5]。
- **比例论表述**：给定两个不等的量，可以找到两条不等的直线，使较大的直线与较小的直线之比小于……（此为欧多克索斯比例论中关于「比」的定义的一部分）[3]。

这些表述的共同内核是：累加操作足以跨越任意给定的界限。这一性质在实数系的构造、极限理论、测度论以及非标准分析（以无穷小为对象的理论）的讨论中都占据核心地位。

## 历史渊源：欧多克索斯的优先权

研究来源一致指出，这条公理的最初表述属于欧多克索斯：

- MathWorld 及密歇根州立大学档案条目均称，该引理「survives in the writings of Eudoxus」，即它保存在欧多克索斯的著作中，可追溯至 Boyer 与 Merzbach（1991）等数学史著作 [1][5]。
- 中文资料进一步明确：历史上首先公布它的是希腊数学家欧多克索斯，早于阿基米德约 100 年；阿基米德本人在手稿中也承认了这一点，但遵从传统，一般仍称之为「阿基米德公理（性质）」 [7]。
- 欧多克索斯公理是其「比例论」（theory of proportions）的一个组成部分 [2]。

因此，这条公理在数学史上是一个典型的「以使用者/传播者命名、而非以首创者命名」的案例。

## 命名的历史：Otto Stolz

据英文维基百科，是 Otto Stolz 将「阿基米德的名字」正式赋予这条公理，从而确立了「阿基米德公理／阿基米德性质」这一术语 [14]。这说明「阿基米德」这一命名并非古代既有，而是在 19 世纪的数学基础研究中被固定下来的。

## 与其他公理及数学基础的关系

### 与 Hilbert 完备性公理的关系

Hilbert 的公理体系中包含一条「完备性公理」（completeness axiom），它的含义常被误解。研究表明：

- Hilbert 的完备性公理 **并非** 指演绎完备性（deductive completeness），而是指「极大性」（maximality）——即其公理系统（第 I–V 组，其中第 V 组为阿基米德性）的模型不能……[13][15]。
- 用现代语言说，阿基米德公理把直线限制到实数的子域上；而极大性（完备性公理）则断言「所有实数都在其中」，从而唯一确定到实数域 [12][15]。

换言之，**阿基米德公理保证了「没有无穷小/无穷大」，而完备性公理则进一步保证了「实数系的全部元素都被包含」**。二者性质不同、作用互补：前者是一个「排无穷」的条件，后者是一个「求极大」的条件 [12][15]。

### Hilbert 关于范畴性与完备性的元理论工作

有研究专门分析了 Hilbert 早期对「范畴性」（categoricity）这一元理论概念的贡献，及其与其他完备性概念的关系 [11]。这为理解阿基米德公理在 Hilbert 公理化方案中的位置提供了背景。

### Otto Hölder 的认识论视角

在 Otto Hölder 关于几何与测量的认识论研究中，阿基米德公理被表述为：给定两个量 $a$ 与 $b$，且 $a < b$，则存在自然数 $m \in \mathbb{N}$ 使 $ma > b$ [4]。Hölder 的工作把这条公理与「测量」这一认识论问题联系起来，说明它不仅是纯数学的命题，也涉及量的可度量性这一更广泛的问题 [4]。

## 矛盾与空白

- **命名归属与首创者分离**：各来源一致承认欧多克索斯的优先地位，同时又保留「阿基米德」之名 [1][5][7]。这一「名不副实」在史料中并不构成矛盾，但读者需注意区分「谁命名」与「谁首创」。
- **「连续性公理」这一别名的恰当性**：部分来源将阿基米德公理等同于「连续性公理」[1][5]，但从现代观点看，阿基米德性质只是完备性的必要条件而非充分条件——一个有序域可以满足阿基米德性质却不完备。因此把它称为「连续性公理」在严格意义上易生歧义，需与 Dedekind 完备性等概念加以区分。
- **公理的多种等价表述之间的精确对应关系**：来源 [3] 给出的古典几何表述带有省略与含糊（「小于……之比」），其与 [4] 的代数表述之间的严格等价性缺乏直接来源论证，存在空白。
- **Hilbert 完备性公理与阿基米德公理的确切关系**：来源 [12][13][15] 提出要点，但对形式化证明的细节着墨不多，仍有待进一步查证。

## 建议补充的来源

1. **Euclid《几何原本》第五卷**（比例论）——用以确认欧多克索斯比例论中「比」的定义与阿基米德公理的原始出处。
2. **Boyer & Merzbach,《A History of Mathematics》**——来源 [1][5] 已引用，但需查阅原书以核实确切页码与表述。
3. **Otto Stolz 原始论文**——用以确证「阿基米德性质」这一命名的确切提出时间与语境。
4. **Hilbert《几何基础》（Grundlagen der Geometrie）**——第 V 组公理（连续性公理组）的原文。
5. **关于非标准分析与无穷小的文献**——用以说明阿基米德公理在「排无穷小」意义上的现代意义。
6. **Hölder 的几何与测量认识论专著**——深化 [4] 所述的认识论视角。

## 小结

阿基米德与「阿基米德公理」的关系，本质上是一种 **传承与命名** 的关系，而非首创关系。这条公理的思想源头在欧多克索斯的比例论，经阿基米德的使用与传播而广为人知，最终由 Otto Stolz 在近代正式命名为「阿基米德公理」。它在现代数学中既是实数系的基本性质之一，也是 Hilbert 公理化体系中「阿基米德性」与「完备性」两条性质相互区分、相互补充的关键环节。

## References

1. [Archimedes' Axiom -- from Wolfram MathWorld](https://mathworld.wolfram.com/ArchimedesAxiom.html) — mathworld.wolfram.com
2. [I invite you to read this paper (Eudoxus' Axiom and Archimedes ...](https://www.freemathhelp.com/forum/threads/i-invite-you-to-read-this-paper-eudoxus-axiom-and-archimedes-lemma-and-share-your-thoughts.136423/) — freemathhelp.com
3. [[PDF] EUDOXUS' AXIOM AND ARCHIMEDES' LEMMA](http://users.uoa.gr/~apgiannop/Sources/Hjelmslev-1950-Centaurus.pdf) — users.uoa.gr
4. [Geometry and Measurement in Otto Hölder's Epistemology](https://journals.openedition.org/philosophiascientiae/832?lang=en) — journals.openedition.org
5. [Archimedes' Lemma](https://archive.lib.msu.edu/crcmath/math/math/a/a311.htm) — archive.lib.msu.edu
6. [阿基米德- 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/%E9%98%BF%E5%9F%BA%E7%B1%B3%E5%BE%B7) — zh.wikipedia.org
7. [阿基米德公理_百度百科](https://baike.baidu.com/item/%E9%98%BF%E5%9F%BA%E7%B1%B3%E5%BE%B7%E5%85%AC%E7%90%86/1797603) — baike.baidu.com
8. [阿基米德：数学之神 - 三联生活周刊](https://www.lifeweek.com.cn/article/40161) — lifeweek.com.cn
9. [阿基米德- 翰林雲端學院](https://www.ehanlin.com.tw/app/keyword/%E5%9C%8B%E4%B8%AD/%E6%AD%B7%E5%8F%B2/%E9%98%BF%E5%9F%BA%E7%B1%B3%E5%BE%B7.html) — ehanlin.com.tw
10. [阿基米德(Archimedes) - 臺灣大學科學教育發展中心](https://case.ntu.edu.tw/highscope/%E9%98%BF%E5%9F%BA%E7%B1%B3%E5%BE%B7-archimedes/index.html) — case.ntu.edu.tw
11. [Hilbert on categoricity and completeness - Springer Nature](https://link.springer.com/article/10.1007/s11229-025-05345-4) — link.springer.com
12. [What is the real meaning of Hilbert's axiom of completeness](https://math.stackexchange.com/questions/808379/what-is-the-real-meaning-of-hilberts-axiom-of-completeness) — math.stackexchange.com
13. [Logical completeness of Hilbert system of axioms - MathOverflow](https://mathoverflow.net/questions/351908/logical-completeness-of-hilbert-system-of-axioms) — mathoverflow.net
14. [Archimedean property - Wikipedia](https://en.wikipedia.org/wiki/Archimedean_property) — en.wikipedia.org
15. [[PDF] Archimedes – Descartes – Hilbert – Tarski - University of Illinois Chicago](https://www.math.uic.edu/~jbaldwin/pub/axconIIfinbib.pdf) — math.uic.edu

## Related
- [[queries/research-326-希尔伯特平行公理与非欧几何的衔接-2026-09-27-153909-research-120]]
