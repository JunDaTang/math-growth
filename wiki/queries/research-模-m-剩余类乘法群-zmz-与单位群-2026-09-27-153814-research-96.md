---
type: query
title: "Research: 模 m 剩余类乘法群 (Z/mZ)* 与单位群"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 模 m 剩余类乘法群 (Z/mZ)* 与单位群

# 模 m 剩余类乘法群 (Z/mZ)* 与单位群

## 概述

在模运算体系中，取集合 $\{0,1,\dots,n-1\}$ 中所有与 $n$ 互质（relatively prime, coprime）的整数，在“模 $n$ 乘法”这一运算下，它们构成一个群，称为**模 $n$ 整数乘法群**（multiplicative group of integers modulo $n$）[6]。由于该集合的元素恰好是模 $n$ 下可逆的剩余类，它又有“模 $n$ 的**既约剩余类**（原剩余类，primitive residue classes）”之称 [4][6]。

在环论（抽象代数的分支）的视角下，该群正是**模 $n$ 整数环 $\mathbb{Z}/n\mathbb{Z}$ 的单位群（group of units）**，即环中所有乘法单位元（可逆元）构成的群 [1][6]。这也解释了它为何常被记作 $(\mathbb{Z}/n\mathbb{Z})^\times$，以及后续的 RSA 等公钥密码系统为何以它为基石 [2][6]。

## 记号

不同的作者对该群采用不同的记号 [6]：

$$(\mathbb{Z}/n\mathbb{Z})^\times,\quad (\mathbb{Z}/n\mathbb{Z})^{*},\quad \mathrm{U}(\mathbb{Z}/n\mathbb{Z}),\quad \mathrm{E}(\mathbb{Z}/n\mathbb{Z}),\quad \mathbb{Z}_n^{*}$$

其中 $\mathrm{E}(\mathbb{Z}/n\mathbb{Z})$ 中的 E 源自德语 *Einheit*（单位），与英文 unit 对应 [6]。中文文献中多直接记作 $(\mathbb{Z}/n\mathbb{Z})^\times$ [3]，或按剩余类的语言称为“mod $n$ 的既约剩余类（群）” [4]。

## 群公理的验证

[6] 给出的标准证明可概括为三步：

1. **互质性的良定义**：若 $a \equiv b \pmod n$，则 $\gcd(a,n)=\gcd(b,n)$，因此“与 $n$ 互质的同余类”这一说法与代表元的选取无关。
2. **乘法与同余类相容**：若 $a\equiv a'$、$b\equiv b'\pmod n$，则 $ab\equiv a'b'\pmod n$，故模 $n$ 乘法在剩余类上良定义。
3. **逆元的存在性**：整数组 $a$ 模 $n$ 可逆当且仅当 $\gcd(a,n)=1$；其模 $n$ 乘法逆元是满足 $ax\equiv 1\pmod n$ 的整数 $x$ [6][9]。

第 3 点实为线性同余定理（Linear Congruence Theorem）的直接推论，也被多次用作“$a$ 可逆 $\Leftrightarrow \gcd(a,n)=1$”的等价判据 [7][9]。综合以上三点，$(\mathbb{Z}/n\mathbb{Z})^\times$ 满足群公理；并且由于整数乘法交换，它是一个**阿贝尔群** [2]。

## 阶与欧拉函数

该群的阶（元素个数）等于 $\{0,1,\dots,n-1\}$ 中与 $n$ 互质的整数个数，由**欧拉函数**（Euler's totient function）$\varphi(n)$ 给出 [6]：

$$|(\mathbb{Z}/n\mathbb{Z})^\times| = \varphi(n)$$

在 OEIS 中该序列编号为 [A000010](https://oeis.org/A000010) [6]。这一事实是多方独立确认的：欧拉函数本身就是“模 $n$ 的同余类所构成的乘法群（即环 $\mathbb{Z}/n\mathbb{Z}$ 的所有单位元组成的乘法群）的阶” [1]；中文介绍亦指出模 $n$ 乘法群“由所有小于 $n$ 且与 $n$ 互质的正整数构成……其阶由欧拉总计函数 $\varphi(n)$ 给出” [2]；教材性材料的表述也是“模 $n$ 的剩余类在乘法下构成群，其阶恰为 $\varphi(n)$” [3]。

## 结构

- **有限交换群**：$(\mathbb{Z}/n\mathbb{Z})^\times$ 是有限阿贝尔群 [2]，其阶为 $\varphi(n)$（见上节）。
- **分解为素幂因子**：当 $m=p_1^{e_1}\cdots p_r^{e_r}$ 时，借助中国剩余定理（下文）可将其视为各素幂分量的乘积 [13]。
- **素数情形**：当 $p$ 为素数时，$(\mathbb{Z}/p\mathbb{Z})^\times$ 的阶为 $p-1$，是一个循环群；这正是欧拉定理群论证明中使用的关键事实——所有 mod $p$ 的非零余数构成阶为 $p-1$ 的乘法群 [4]。

> 说明：现有资料 [6][13] 讨论了商（平方剩余）与单位群的计数，但**未系统给出 $(\mathbb{Z}/n\mathbb{Z})^\times$ 何时循环（即原根存在性）的完整刻画**，也未涉及 Carmichael 函数 $\lambda(n)$。这一空白见下文“争议与空白”一节。

## 与中国剩余定理的联系

**中国剩余定理**（Chinese remainder theorem，又称孙子定理 [5][11]）断言：若 $n_i$ 两两互质，且 $0\le a_i < n_i$，则存在唯一满足 $0\le x<N$（$N=\prod n_i$）且 $x$ 除以 $n_i$ 余 $a_i$ 的整数 $x$ [11]。其原始表述见于《孙子算经》中的同余问题（如 $x\equiv 2\pmod 3,\equiv 3\pmod 5,\equiv 2\pmod 7$，解为 $x=23+105k$）[11]。有资料指出，中国剩余定理（孙子定理）是同余理论的中心定理之一 [5]。

在群与环的层面，中国剩余定理通常被视为**环的同构**而非仅仅是循环群的同构 [12]，即当 $m,n$ 互质时：

$$(\mathbb{Z}/mn\mathbb{Z}) \;\cong\; (\mathbb{Z}/m\mathbb{Z}) \times (\mathbb{Z}/n\mathbb{Z})$$

由此导出**欧拉函数的乘性**：对互质的正整数 $m,n$，有 $\varphi(mn)=\varphi(m)\varphi(n)$ [13]。Keith Conrad 的讲义以 $U_m=\{a\bmod m: (a,m)=1\}$ 等记号，通过构造映射
$f: U_{mn}\to U_m\times U_n$，$c\bmod mn \mapsto (c\bmod m,\, c\bmod n)$
证明两集合等势，从而证得该乘性公式；例如 $U_3=\{1,2\}$、$U_5=\{1,2,3,4\}$、$U_{15}=\{1,2,4,7,8,11,13,14\}$，而 $|U_{15}|=\varphi(15)=\varphi(3)\varphi(5)=2\times 4=8$ [13]。

此外，Conrad 的讲义还用中国剩余定理处理“模 $m$ 的平方剩余个数 $|S_m|$”的乘性（$|S_{mn}|=|S_m||S_n|$），并给出 $S_3=\{0,1\}$、$S_5=\{0,1,4\}$、$S_{15}=\{0,1,4,6,9,10\}$ 等例证 [13]。多个来源同时强调：中国剩余定理能将对一般模数的同余问题，化归为对若干较小模数（往往是素幂）的同类问题 [11][13][15]。

## 相关定理与应用

- **欧拉定理**：对 $\gcd(a,n)=1$，有 $a^{\varphi(n)}\equiv 1\pmod n$。其群论证明的关键在于 $a$ 在乘法群 $(\mathbb{Z}/n\mathbb{Z})^\times$ 中的阶整除 $\varphi(n)$（拉格朗日定理）[1][4]。部分材料称其为“欧拉数论定理”，并指出其证明依赖于 mod $n$ 既约剩余类构成群这一事实 [4]。
- **费马小定理**：当 $n=p$ 为素数时，$\varphi(p)=p-1$，欧拉定理退化为 $a^{p-1}\equiv 1\pmod p$；相关资料将其与单位群、可逆元判据归入同一主题 [9]。相关数学家见 [[费马]]。
- **公钥密码学**：模 $n$ 乘法群的阶由 $\varphi(n)$ 给出，这使其成为 **RSA 等公钥密码系统**的理论基础 [2]；从“代数结构视角”看，模 $n$ 剩余类在乘法下构成群 $(\mathbb{Z}/n\mathbb{Z})^\times$，其阶恰为 $\varphi(n)$，这正是数论与密码学之间的桥梁 [3]。
- **中国剩余定理的计算用途**：它被广泛用于大整数计算，能把一个已知结果大小上界的大计算，替换为若干个小整数上的同类计算 [11]。

## 与既有知识脉络的关联

本 wiki 此前主要围绕《数学指南——实用数学手册》的[[数理统计]]、[[概率空间]]、[[测度论]]、[[科尔莫戈罗夫公理化概率论]]等页面展开，模运算与抽象代数尚未成体系覆盖。本篇所整理的 $(\mathbb{Z}/n\mathbb{Z})^\times$ 属于代数数论/抽象代数方向，可作为后续“同余理论”“群论基础”等条目的锚点。运算的良定义、单位群的构造与概率论中[[事件域]]、[[概率测度]]所依赖的测度论抽象同属“用公理化结构刻画对象”的方法论，但两者并无直接内容依赖。

## 争议与空白

1. **记号不统一**：同一对象至少有 $(\mathbb{Z}/n\mathbb{Z})^\times$、$(\mathbb{Z}/n\mathbb{Z})^{*}$、$\mathrm{U}(\mathbb{Z}/n\mathbb{Z})$、$\mathrm{E}(\mathbb{Z}/n\mathbb{Z})$、$\mathbb{Z}_n^{*}$ 等写法 [6]，阅读时需注意上下文对“$*$”与“$\times$”的使用是否均表示单位群。
2. **原根与循环性未被覆盖**：现有资料确认了素数情形的循环性 [4]，但**未给出 $(\mathbb{Z}/n\mathbb{Z})^\times$ 对一般 $n$ 何时为循环群的完整定理**（即原根存在性的判别），亦未引入 Carmichael 函数。这是本主题最明显的知识缺口。
3. **源文本质量问题**：来源 [13] 为 PDF 转换文本，存在大量 OCR 讹误（如把 $\gcd$ 写作 $(m_i,m_j)$、把 $\varphi$ 写作 `’`、数学符号断裂），引用时须结合上下文判断；来源 [11] 的维基条目摘录不完整，仅保留定理陈述与用途。
4. **中文术语译名分歧**：$(\mathbb{Z}/n\mathbb{Z})^\times$ 有“乘法群”“单位群”“既约剩余类群”“原剩余类群”等多种叫法 [2][4][6]，中文语境下未见统一规范。

## 建议补充来源

- **原根与循环性**：关于 $(\mathbb{Z}/n\mathbb{Z})^\times$ 何时循环（$n=1,2,4,p^k,2p^k$）的标准定理，可查任一初等数论教材（如 Ireland & Rosen、Niven–Zuckerman–Montgomery）。
- **Carmichael 函数 $\lambda(n)$**：作为“群指数”的刻画，与欧拉函数 $\varphi(n)$ 常被并列讨论。
- **群阶的拉格朗日定理**：欧拉定理群论证明所依赖的通用群论工具 [1][4]，建议单独立条。
- **RSA 与离散对数**：将本群作为计算数论应用（模幂、模逆、离散对数）的入口 [2][3]。
- **中国剩余定理的环论证明**：更一般形式的同构 $\mathbb{Z}/(I_1\cap\cdots\cap I_n)\cong\prod \mathbb{Z}/I_i$，见 [12][15]。
- **《数学指南——实用数学手册》对应章节**：本 wiki 已有该书 6.2、6.3 各节页面（如 [[10-数学指南实用数学手册--18-62-科尔莫戈罗夫的概率论公理化基础--fv9q82]]），若该书含同余/代数章节，宜补录以在同一知识体系内建立交叉链接。

## 关键结论速览

| 命题 | 内容 | 来源 |
|---|---|---|
| 群的定义 | $\{a\bmod n:(a,n)=1\}$ 在模 $n$ 乘法下成群 | [6][2] |
| 可逆判据 | $a$ 模 $n$ 可逆 $\iff \gcd(a,n)=1$ | [6][7][9] |
| 群的阶 | $\lvert(\mathbb{Z}/n\mathbb{Z})^\times\rvert=\varphi(n)$ | [1][2][3][6] |
| 交换性 | 该群是有限阿贝尔群 | [2] |
| 乘性 | $\gcd(m,n)=1\Rightarrow\varphi(mn)=\varphi(m)\varphi(n)$ | [13] |
| 欧拉定理 | $\gcd(a,n)=1\Rightarrow a^{\varphi(n)}\equiv 1\pmod n$ | [1][4] |
| 分解 | $(\mathbb{Z}/mn\mathbb{Z})\cong(\mathbb{Z}/m\mathbb{Z})\times(\mathbb{Z}/n\mathbb{Z})$ | [12][13] |

## References

1. [欧拉函数- 维基百科，自由的百科全书](https://zh.wikipedia.org/wiki/%E6%AD%90%E6%8B%89%CF%86%E5%87%BD%E6%95%B8) — zh.wikipedia.org
2. [模n整数乘法群| Bohrium](https://www.bohrium.com/sciencepedia/feynman/keyword/multiplicative_group) — bohrium.com
3. [質數、同餘與密碼學：藏在那把鎖裡的數論 - Uedu](https://uedu.tw/math/a/number-theory) — uedu.tw
4. [扒一扒那些叫欧拉的定理们（十一）——欧拉数论定理](https://zhuanlan.zhihu.com/p/412746705) — zhuanlan.zhihu.com
5. [[PDF] 代数学基础 - 中国科学技术大学](http://staff.ustc.edu.cn/~msheng/references/alg-Intro.pdf) — staff.ustc.edu.cn
6. [Multiplicative group of integers modulo n - Wikipedia](https://en.wikipedia.org/wiki/Multiplicative_group_of_integers_modulo_n) — en.wikipedia.org
7. [Proof that the multiplicative group of integers modulo n is a group](https://math.stackexchange.com/questions/780189/proof-that-the-multiplicative-group-of-integers-modulo-n-is-a-group) — math.stackexchange.com
9. [The Integers modulo n. The Group of Units. Fermat's Theorem.](https://justtothepoint.com/algebra/groupunits/) — justtothepoint.com
11. [Chinese remainder theorem - Wikipedia](https://en.wikipedia.org/wiki/Chinese_remainder_theorem) — en.wikipedia.org
12. [Analog to the Chinese Remainder Theorem in groups other than Z_n.](https://mathoverflow.net/questions/18893/analog-to-the-chinese-remainder-theorem-in-groups-other-than-z-n) — mathoverflow.net
13. [[PDF] Chinese remainder theorem - Keith Conrad](https://kconrad.math.uconn.edu/blurbs/ugradnumthy/crt.pdf) — kconrad.math.uconn.edu
15. [Chinese Remainder theorem on the ring of integers modulo n](https://math.stackexchange.com/questions/3559133/chinese-remainder-theorem-on-the-ring-of-integers-modulo-n) — math.stackexchange.com
