---
type: query
title: "Research: 手册 1.3.1.4 节（$o(\\cdots)$ 记号的定义）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 手册 1.3.1.4 节（$o(\cdots)$ 记号的定义）

# 手册 1.3.1.4 节：$o(\cdots)$ 记号的定义

## 概要

本页汇总关于 [[小o记号]]（little-o，$o(\cdots)$）定义的若干外部资料，用以对照 [[数学指南实用数学手册]] 第 1.3.1.4 节的相应定义。§1.3.1.4 讨论的是如何用 $o(\cdots)$ 描述一个函数「渐近地远小于」另一个函数；这一记号与手册 0.7.3 节 [[渐近级数]] 中所用的 $o(\cdots)$ 属于同一符号体系，也与 [[渐近等式]]（$\cong$）、[[庞加莱渐近展开式]]（$\sim$）构成一组渐近比较工具。

需要说明的是：手册 1.3.1.4 节的正文本身尚未入库，本页的内容主要来自外部网络资料 [1]–[14]，属于「外部定义—手册定义」的对照性整理，而非对手册原文的转述。

## 形式定义

### 无穷远点处（$x\to\infty$）

各来源对 $o$ 的定义高度一致。形式化地，$f(x)=o(g(x))$（当 $x\to\infty$）当且仅当：对**每一个** $C>0$，存在实数 $N$，使得对所有 $x>N$ 都有 $|f(x)|<C\,|g(x)|$；若 $g(x)\neq 0$，这等价于

$$\lim_{x\to\infty}\frac{f(x)}{g(x)}=0 .$$

[6] 这一表述与 $\varepsilon$–$N$ 语言下的极限定义完全对应，因而也被视为 $o$ 记号最「干净」的定义形式。

### 有限点处（$x\to a$）

对实数点 $a$，同样可写 $f(x)=o(g(x))$（当 $x\to a$）：对每个 $C>0$，存在正实数 $\delta$，使得对所有满足 $|x-a|<\delta$ 的 $x$ 都有 $|f(x)|<C\,|g(x)|$；当 $g(x)\neq 0$ 时等价于 $\lim_{x\to a} f(x)/g(x)=0$。[6] 这说明 $o$ 记号并不专属于无穷远点，也可用于 $x\to 0$ 等情形——[7] 给出的图示即以 $x\to 0$ 为例，指出此时 $1 \gg x \gg x^{2} \gg x^{3}$，故可写 $f(x)=O(1)$（$x\to 0$）。

### 一般拓扑/度量空间上的推广

[13] 给出更一般的框架：设 $(M,d)$ 为度量空间，$X\subset M$，$x_0\in\mathrm{acc}(X)$，$f,g:X\to\mathbb{K}^n$，在 $X\cap U_\delta(x_0)$ 上用范数 $\|\cdot\|$ 控制，则可定义相应的 $O$ 与 $o$ 关系。这一推广说明手册式的 $o$ 定义（通常限制在实变量或复变量的一维情形）只是更普遍定义的特例。

## 与 Big-O 的关系：严格性与强弱

若干来源集中论述了 $o$ 与 $O$ 的核心差别：

- **量词不同**：Big-O 只需「对**某个**常数 $c$ 成立」，little-o 则要求「对**任何**常数 $c$ 都成立」，因此 little-o 是比 Big-O **更强**的条件 [1][6]。
- **蕴含关系**：$f(x)=o(\varphi(x))$ 蕴含且强于 $f(x)=O(\varphi(x))$ [9]。
- **严格小于 vs 非严格**：$o$ 表示「严格小于的上界」，即函数渐进地小于另一个函数，不含「等于」的情形 [2][3][5]。百科类资料给出的记忆法是：含等于（非严格）用大写，不含等于（严格）用小写——相等是 $\Theta$、小于是 $O$、大于是 $\Omega$ [5]。
- **常数可提取**：由于极限中的常数可提出，若 $f=o(x^{n})$，则对任意 $n!$ 之类的常数因子仍有 $f=o(x^{n}/n!)$（在极限存在的前提下）[4]。这解释了为什么渐近级数中 $o$ 项的常数倍不影响其阶的判定。

## 与其他渐近符号的对照

| 记号 | 含义 | 类比（算法语境） |
|---|---|---|
| $f=O(g)$ | 渐近上界（$\exists c,n_0$，$0\le f\le cg$） | ≤ |
| $f=o(g)$ | 严格上界（$f/g\to 0$） | < |
| $f=\Omega(g)$ | 渐近下界（$0\le cg\le f$） | ≥ |
| $f=\omega(g)$ | 严格下界（$0<cg<f$） | > |
| $f=\Theta(g)$ | 渐近紧确界（$c_1g\le f\le c_2g$） | = |

表格依据 [5][6]。此外，[8] 指出 $\Omega$（在「不是 $o$ 的」意义上）由 [[queries/哈代|Hardy]] 与 Littlewood 于 1914 年引入，$\Omega_R$、$\Omega_L$（今记 $\Omega_+$、$\Omega_-$）则于 1916 年引入；而 $\sim$ 的现代定义由 Landau（1909）与 Hardy（1910）给出，另有钱 $f\asymp g$（$f=O(g)$ 且 $g=O(f)$）。这些记号在本 wiki 中分别对应 [[渐近等式]] 与 [[庞加莱渐近展开式]]。

## 命名与历史沿革

- **字母 O 的由来**：$O$ 常被称为 Landau 符号（Landau's symbol），源自德国数论学家 [[queries/朗道|Edmund Landau]]；字母 $O$ 取自「阶」（order）一词，因为函数的增长率也称其阶 [6]。
- **首次提出**：多数来源认为 $O$ 记号由 Paul Bachmann 于 1894 年在《Analytische Zahlentheorie》第二卷中首次引入，Landau 随后采用 [8][14]；但 [5] 记为 1892 年，存在年份出入。
- **$o$ 的引入**：$o$ 记号确由 Landau 引入，用以取代更早的记号 $\{x\}$（Narkiewicz 2000, p. XI）[14]；Wikipedia 与 MathWorld 均记为 1909 年 [8][14]，而 [12] 记为 1905 年。
- **合称**：$O$ 与 $o$ 两者现统称 Landau symbols [6][8]；[11] 亦以「Landau-Symbole」称之，用于数学与计算机科学中描述函数与序列的渐近行为。

## 在算法复杂度分析中的用法

在计算机科学语境下，$o$ 记号通常用于刻画「严格更好」的界。例如比较排序算法的时间复杂度至少为 $\Omega(n\log n)$ [3]；而 $o$ 用于表达「严格小于」的上界，例如某算法的时间是 $o(n^2)$ 但非 $O(n\log n)$ 之类的精细区分。分析中常用的数量级包括 $O(1)$、$O(\log n)$、$O(n)$、$O(n\log n)$、$O(n^2)$、$O(2^n)$、$O(n!)$，通常只关注最高阶项 [5]。

## 与本站既有页面的衔接

- [[小o记号]]：本主题的在站概念页，应与本节定义相互印证。
- [[渐近级数]]、[[10-数学指南实用数学手册--8-073-渐近级数--1jby90l]]：手册 0.7.3 节大量使用 $o(\cdots)$ 书写余项。
- [[渐近等式]]、[[庞加莱渐近展开式]]：同属渐近比较符号族。
- [[庞加莱]]：庞加莱的意义是渐近展开理论的命名者（与 $o$ 的历史无直接关系，但常并列出现）。
- [[数学指南实用数学手册]]：本节的所属著作。

## 矛盾、缺口与待补来源

1. **年份矛盾**：Big-O 的首次提出年份有 1892 [5] 与 1894 [8][14] 两种说法；$o$ 的引入年份有 1905 [12] 与 1909 [8][14] 两种说法。可能前者分别指书稿完成与出版年份，需以 Bachmann《Analytische Zahlentheorie》第二卷与 Landau《Handbuch der Lehre von der Verteilung der Primzahlen》（1909）原书核对。
2. **手册原文缺位**：手册 1.3.1.4 节正文尚未入库，无法直接确认手册使用的是「$\forall C>0$」式量词定义还是「$\lim f/g=0$」式极限定义，也未确认其是否限定于 $x\to\infty$。同类情况可参见 [[手册113213节尚未入库]] 与 [[手册1101与1106收敛条目缺失]]。
3. **符号体系一致性**：手册 0.7.3 节同时使用 $\cong$ 与 $\sim$，而外部资料 [8] 强调 $\sim$（Landau 1909/Hardy 1910）与 $o$（Landau 1909）同年确立；建议核对手册 1.3.1.4 是否明确区分 $o$ 与 $\sim$ 的强弱，以及与 [[渐近等式]] 中 $\cong$ 的关系。
4. **建议补充来源**：Hardy & Wright, *An Introduction to the Theory of Numbers* §1.6（pp. 7–8）；de Bruijn, *Asymptotic Methods in Analysis*（pp. 3–10）；Landau 1909 原书；以及手册 1.3 节其余小节（1.3.1.1–1.3.1.3）的原文，以便恢复完整的符号定义上下文。

## 参考文献

[1] r/learnmath, "Big O vs little O 符号"（reddit.com）
[2] CSDN, 《算法分析之常用符号大O、小o、大Ω符号、大Θ符号、w符号》
[3] 知乎专栏, 《算法分析中的符号表示：大小O、大小Omega 及大Theta》
[4] r/math, "小o/大O 符号（泰勒级数）"（reddit.com）
[5] 百度百科, 「大O表示法」
[6] MIT, "Big O notation (Landau's symbol)"（web.mit.edu）
[7] Statistics How To, "Big O Notation (Landau's Symbol)/Order of a Function"
[8] Wikipedia, "Big O notation"
[9] Appalachian State University, "Asymptotic Notation"（cs.appstate.edu）
[10] extremalcombinatorics.com, "Appendix A Asymptotic Notation"
[11] biancahoegel.com, "Landau-Symbole"
[12] Spektrum, *Lexikon der Mathematik*, "Landau-Symbole"
[13] Universität Stuttgart, "Die Definition der Landau-Symbole"
[14] Wolfram MathWorld, "Landau Symbols"

## References

1. [Big O vs little O 符号: r/learnmath](https://www.reddit.com/r/learnmath/comments/ipv4jg/big_o_vs_little_o_notation?tl=zh-hans) — reddit.com
2. [算法分析之常用符号大O、小o、大Ω符号、大Θ符号、w符号原创](https://blog.csdn.net/qq_39745932/article/details/82747191) — blog.csdn.net
3. [算法分析中的符号表示：大小O、大小Omega 及大Theta](https://zhuanlan.zhihu.com/p/14494506752) — zhuanlan.zhihu.com
4. [小o/大O 符号（泰勒级数） : r/math](https://www.reddit.com/r/math/comments/4u0ibh/little_obig_o_notation_taylor_series?tl=zh-hans) — reddit.com
5. [大O表示法](https://baike.baidu.com/item/%E5%A4%A7O%E8%A1%A8%E7%A4%BA%E6%B3%95/1851162) — baike.baidu.com
6. [Big O notation (with a capital letter O, not a zero), also ...](https://web.mit.edu/16.070/www/lecture/big_o.pdf) — web.mit.edu
7. [Big O Notation (Landau's Symbol)/Order of a Function - Statistics How To](https://www.statisticshowto.com/big-o-notation-landaus-symbol) — statisticshowto.com
8. [Big O notation - Wikipedia](https://en.wikipedia.org/wiki/Big_O_notation) — en.wikipedia.org
9. [Asymptotic Notation](https://cs.appstate.edu/wmcb/Class/2310/LandauNotation.pdf) — cs.appstate.edu
10. [Appendix A Asymptotic Notation](https://extremalcombinatorics.com/notes/app_asymp.html) — extremalcombinatorics.com
11. [Landau-Symbole](http://biancahoegel.com/mathe/operator/landau-symbole.htm) — biancahoegel.com
12. [Lexikon der Mathematik - : - Landau-Symbole](https://www.spektrum.de/lexikon/mathematik/landau-symbole/5790) — spektrum.de
13. [Die Definition der Landau-Symbole.](https://pnp.mathematik.uni-stuttgart.de/iadm/Weidl/ana1-13-14/skript/skriptsu114.html) — pnp.mathematik.uni-stuttgart.de
14. [Landau Symbols -- from Wolfram MathWorld](https://mathworld.wolfram.com/LandauSymbols.html) — mathworld.wolfram.com
