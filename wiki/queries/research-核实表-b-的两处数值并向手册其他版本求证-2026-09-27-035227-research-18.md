---
type: query
title: "Research: 核实表 b 的两处数值并向手册其他版本求证"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 核实表 b 的两处数值并向手册其他版本求证

# 核实表 b 的两处数值并向手册其他版本求证

## 研究背景

在 [[数学指南实用数学手册]] 的 0.5.4 节「椭圆积分」中，表 b 给出第二类椭圆积分 $E(\varphi, k)$ 的数值（见 [[表b第二类椭圆积分]] 与 [[第二类椭圆积分]]）。此前已在 [[表b中两处数值的排版讹误]] 中记录该表两处数值疑似排版讹误。本页汇总围绕该疑点的核实工作：一方面寻找可独立比对的外部数值表，另一方面考察手册不同版本之间是否存在文本差异，以判断讹误究竟来自源文献、译本还是中译转写。相关的表号标注与相邻小节问题另见 [[三张椭圆积分表的表号未标注]] 与 [[queries/手册1.14.19节尚未入库]]。

## 手册的版本谱系

要谈「向其他版本求证」，必须先把可比的版本厘清：

- 原始底本是 Bronstein 与 Semendjajew 的俄文《数学手册》，苏联初版于 1945 年 [4]。
- 1958 年由 Viktor Ziegler 译成德文，在 Leipzig 的 B. G. Teubner 出版；到 1978 年已累计 18 版 [2][4]。
- 1979 年在 Günter Grosche 与 Ziegler 主持下，由东德多所高校数学家参与，出版全面修订的第 19 版 [2][4]。
- 此后由 Eberhard Zeidler 主持，Springer（承继 Teubner）出版四卷本《Teubner-Taschenbuch der Mathematik》/《Springer-Taschenbuch der Mathematik》，按 [4] 的说法属于「完全重编」，其覆盖面远超旧的 Bronstein。可查到的版本包括 2003 年 Vieweg+Teubner 版（ISBN 3-322-96782-4）[4] 与 2013 年 Springer 第 2 版（ISBN 9783322967817，1300 页）[2][5]。
- 牛津大学出版社据德文新版出版英译本，并改名为《Oxford User's Guide to Mathematics》[8]。
- 中译本《数学指南——实用数学手册》由李文林等译，科学出版社 2012 年 1 月出版，1303 页，ISBN 978-7-03-032540-2 [6][8][9]。

其中 0.5.4 节对应中译本第 126 页 [10]。

## 版本之间的差异：校勘的关键依据

译者序提供了直接影响核实策略的信息：中译本是在「德文原版与 OUP 英译本相互参校」的基础上完成的，并且明确指出——英译本纠正了德文原版的一些错误，但英译本自身也产生了新的错误，「有的还是比较本质的」[8]。由此可以得出两点：

1. 表 b 中若确有讹误，其来源可能是德文原版、英译本或中译排版三者中的任意一层，不能默认归咎于中译；
2. 单一版本不足以定论，至少需要两个独立版本交叉比对 [8]。

这也解释了为何「向手册其他版本求证」是必要的，而非仅仅重新核对中译本的一页。

## 可用于独立核对的外部数值资料

在无法直接取得德文/英文原书表格时，可借用公开的数值表与公式关系做旁证：

- NASA 的《TABLES OF ELLIPTIC INTEGRALS》收录按模数与振幅展开的椭圆积分数值表，可用于逐点比对 [12]。
- NIST 的文献给出完全椭圆积分 $K$ 的定积分公式与超几何表示，可作为解析校验的补充 [3]。
- netlib 的《2.9 Incomplete Elliptic Integrals》给出 $F(\varphi, k)$、$E(\varphi, k)$、$R_D$、$R_F$ 等函数的数值误差报告，并指出 $F(\varphi, k)$ 的误差在 $\varphi = \pi/2$、$k = 1$ 奇点附近增大 [11]。
- Waterloo 的讲义整理了 $E$、$F$、$D$ 之间的恒等关系（如 $F = E + k^2 D$），可用于检查表内相邻量之间的一致性 [14]。
- Springer 章节「Unvollständige elliptische Integrale」以 Legendre 标准形处理不完全椭圆积分，并指向 Jahnke–Emde《Tafeln höherer Funktionen》（Teubner, Stuttgart）作为数值表来源 [1]。

## 可能的核对路径

结合 [[表b与表c在φ等于90度处的交叉一致]]，表 b 在 $\varphi = 90°$ 处应与表 c（完全椭圆积分，[[表c完全椭圆积分]]、[[完全椭圆积分]]）相符；[[表a与表c在φ等于90度处的交叉一致]] 则提供了同类交叉校验的先例。因此对表 b 的两处可疑值，可先用手册内部的两表交叉一致性判断其是否为孤立异常，再以 [12] 等外部表逐点核对。由于 [[模数与模角]] 与 [[振幅]] 的取值格点在不同资料中未必一致，比对时需注意插值或就近格点的取舍。

## 矛盾与缺口

- 本次检索到的资料均未给出表 b 中那两处具体数值，因而无法在本页完成最终的数值判定。
- 没有任何来源直接复制了德文原版或 OUP 英译本的表 b 内容，「讹误属于哪一版本」的问题仍无实据。
- [8] 关于「英译本引入新错误」的说明是译者序中的概括叙述，未附具体条目，无法据此定位到椭圆积分表。
- [1][2][4][5] 等主要是版本与书目层面的信息，不构成数值证据；它们只能支持「存在可资比对的平行版本」这一前提。

## 建议进一步查找的资料

- 《Oxford User's Guide to Mathematics》原书，核对表 b 对应页。
- 德文《Teubner-Taschenbuch der Mathematik》/《Springer-Taschenbuch der Mathematik》相应表格。
- Abramowitz & Stegun,《Handbook of Mathematical Functions》第 17 章（椭圆积分）。
- Byrd & Friedman,《Handbook of Elliptic Integrals for Engineers and Scientists》。
- Jahnke–Emde,《Tafeln höherer Funktionen》[1]。

## References

1. [Unvollständige elliptische Integrale | Springer Nature Link](https://link.springer.com/chapter/10.1007/978-3-322-89446-5_3) — link.springer.com
2. [Teubner-Taschenbuch der Mathematik - Google Livros](https://books.google.co.mz/books/about/Teubner_Taschenbuch_der_Mathematik.html?hl=pt-PT&id=iRfUBgAAQBAJ) — books.google.co.mz
3. [[PDF] Definite integrals of the complete elliptic integral K](https://nvlpubs.nist.gov/nistpubs/jres/80B/jresv80Bn2p313_A1b.pdf) — nvlpubs.nist.gov
4. [Taschenbuch der Mathematik – Wikipedia](https://de.wikipedia.org/wiki/Taschenbuch_der_Mathematik) — de.wikipedia.org
5. [Springer-Taschenbuch der Mathematik](https://link.springer.com/content/pdf/10.1007/978-3-8348-2359-5.pdf) — link.springer.com
6. [数学指南——实用数学手册](https://baike.baidu.com/item/%E6%95%B0%E5%AD%A6%E6%8C%87%E5%8D%97%E2%80%94%E2%80%94%E5%AE%9E%E7%94%A8%E6%95%B0%E5%AD%A6%E6%89%8B%E5%86%8C/19323750) — baike.baidu.com
8. [遇见你常见你丨《数学指南：实用数学手册》](https://www.sohu.com/a/137148995_410558) — sohu.com
9. [数学指南: 实用数学手册](https://books.google.es/books?id=flOCoAEACAAJ&hl=es&lr=) — books.google.es
10. [数学指南-实用数学手册_目录德国- redufa](https://www.cnblogs.com/redufa/p/18668710) — cnblogs.com
11. [2.9 Incomplete Elliptic Integrals](https://www.netlib.org/math/docpdf/ch02-09.pdf) — netlib.org
12. [TABLES OF ELLIPTIC INTEGRALS](https://ntrs.nasa.gov/api/citations/19650021539/downloads/19650021539.pdf) — ntrs.nasa.gov
14. [Elliptic Integrals, Elliptic Functions and Theta Functions](https://www.mhtlab.uwaterloo.ca/courses/me755/web_chap3.pdf) — mhtlab.uwaterloo.ca

## Related
- [[queries/research-095-小节转写疑误多份清单的合并核对-2026-09-27-073657-research-45]]
- [[queries/research-0174-节双曲线参数方程尚未入库-2026-09-27-040305-research-27]]
