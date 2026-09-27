---
type: query
title: "Research: 自然常数 e（欧拉数）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 自然常数 e（欧拉数）

# 自然常数 e（欧拉数）

## 概述

自然常数 $e$ 是数学中与圆周率 $\pi$、虚数单位 $i$ 并列的基础常数之一，近似值为 $2.718281828459045\ldots$，属于无理数且是超越数 [1][5][6]。它既是自然对数的底，也是唯一使指数函数 $e^x$ 的导数等于自身的正实数底 [6][7][8][9][10]。$e$ 常见于连续复利、人口增长、放射性衰变、热传导、概率论与微分方程等场景 [3][6]，并通过 [[欧拉公式]] 与 [[复数]]、[[复平面]] 发生联系 [6]。

## 名称、符号与历史

### 常见名称

$e$ 在中文资料中常被称为「自然底数」「自然常数」「欧拉数」或「纳皮尔常数」[1][5]。中文维基百科的「欧拉常数」条目会重新导向到 $e$ 的条目 [2]，这为后续的术语辨析埋下歧义。

### 发现与命名史

- 1683 年，雅各布·伯努利（Jacob Bernoulli）在研究连续复利时考察 $(1+1/n)^n$ 当 $n\to\infty$ 的极限，并用二项式定理证明该极限介于 2 与 3 之间，这被认为是 $e$ 的最早近似 [3]。
- 已知最早在文献中使用该常数的是莱布尼茨（Leibniz）于 1690 年和 1691 年写给 [[惠更斯]] 的通信，当时用字母 $b$ 表示 [5]。
- 1727 年 [[欧拉]] 开始用 $e$ 表示该常数；它第一次出现在出版物中是 1736 年欧拉的《力学》（*Mechanica*）[5]。
- 关于为何选用字母 $e$，来源 [5] 坦言「原因确实不明」，一种看法是 $e$ 取自「指数函数」（exponential）的首字母，另一种看法是 $a,b,c,d$ 已有常用含义，而 $e$ 是第一个可用的字母 [5]。
- 来源 [3] 引述的历史说明还提到，伯努利当时并未意识到自己的工作与对数之间的联系 [3]。

### 数值速览

据来源 [4]，$e$ 的前 15 位小数为 $2.71828\,18284\,59045\cdots$；由单调有界性可得 $2\le e<3$ [4]。维基百科条目给出的位数数列编号为 OEIS A001113，连分数（线性表示）为 $[2; 1, 2, 1, 1, 4, 1, 1, 6, 1, 1, 8, 1, 1, 10, \ldots]$ [5]。

## 等价定义

来源 [5] 列出 $e$ 的若干等价定义，并指出这些定义可证明等价（参见「指数函数的特征描述」）：

| 类型 | 定义式 |
| --- | --- |
| 极限 | $e=\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n$，或 $e=\lim_{t\to 0}(1+t)^{1/t}$ |
| 级数 | $e=\sum_{n=0}^{\infty}\frac{1}{n!}=\frac{1}{0!}+\frac{1}{1!}+\frac{1}{2!}+\cdots$ |
| 积分 | $e$ 是唯一正数 $x$ 使 $\int_1^x \frac{\mathrm{d}t}{t}=1$ |
| 导数极限 | $e$ 是唯一实数 $x$ 使 $\lim_{h\to 0}\frac{x^h-1}{h}=1$ |

其中极限定义在上式代表「把 1 与无穷小相加，再自乘无穷多次」[5]。级数定义亦见于 [4][8][10]。

### 极限存在性的初等证明思路

来源 [4] 给出较完整的初等论证：令 $a_n=(1+1/n)^n$，用二项式展开得

$$a_n = 1+1+\frac{1}{2!}\left(1-\frac{1}{n}\right)+\frac{1}{3!}\left(1-\frac{1}{n}\right)\left(1-\frac{2}{n}\right)+\cdots$$

随后证明 $\{a_n\}$ 单调增加，并用 $1/k! < 1/2^{k-1}$ 得到 $a_n<3$，从而由单调有界定理知极限存在，并以 $e$ 表示 [4]。来源 [4] 还给出数值表：$a_{10}\approx 2.5937425$，$a_{100}\approx 2.7048138$，$a_{1000}\approx 2.7169239$，$a_{10000}\approx 2.7181459$。

## 分析学核心性质：$e^x$ 是自身的导数

多个来源共同强调，$e$ 在微积分中的核心意义在于 $\frac{d}{dx}e^x=e^x$：

- 该性质使 $e^x$ 成为「在微分下自我复制」的函数，广泛用于描述动态系统的微分方程，如种群增长、放射性衰变与热传导 [6]。
- 对 $f(x)=e^x$，曲线在任意点处的切线斜率等于该点的高度；$x=0$ 处斜率为 $e^0=1$，$x=1$ 处斜率为 $e^1=e$ [7][8]。
- 一般指数函数 $a^t$ 的导数都与其自身成比例，但只有 $e$ 使比例常数为 1，即只有 $e^t$ 的导数严格等于自身；其他底数可写成 $a^t=e^{t\ln a}$，比例常数为 $\ln a$ [7][9]。
- 也可用 $\exp(x)$ 定义为满足 $\frac{d}{dx}\exp(x)=\exp(x)$ 且 $\exp(0)=1$ 的函数，它与 $e^x$ 相同 [10]。
- 借助二项式定理，$e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}$ 在微积分中经常使用 [10]。

自然对数以 $e$ 为底 [1][4][6]，这也是「自然底数」一名的由来。

## 与 [[欧拉公式]] 及复分析的联系

来源 [6] 将欧拉恒等式

$$e^{i\pi}+1=0$$

列为「数学中最优美的等式之一」，因为它把 $0,1,e,i,\pi$ 五个基本常数联系起来。该等式是 [[欧拉公式]] 的特例，而 $e^z$ 的级数定义使其可以自然地扩展到 [[复平面]]，成为 [[复变函数]] 中指数函数与 [[解析延拓]] 的出发点。需注意，本次收集的来源只给出恒等式的陈述，未展开复指数函数的完整理论。

## 典型应用

- **复利与连续增长**：来源 [3] 以细胞分裂与复利为例说明 $(1+1/n)^n$ 的极限过程；来源 [6] 亦把连续增长列为 $e$ 的起源性应用。
- **自然科学建模**：种群增长、放射性衰变、热传递等由微分方程描述的系统，因 $e^x$ 的自我复制性质而得到简化 [6]。
- **概率与统计**：读者评论提到泊松分布（Poisson distribution）中的 $e$，以及「抽奖」类问题——若单次中奖概率为 $1/n$，抽取 $n$ 次至少中一次的概率趋于 $1-1/e$，抽不中的概率趋于 $1/e$ [3]。这属于科普性说明，需与教材定义相互印证。
- **微积分与微分方程**：$e$ 是求解常微分方程与描述动态系统的核心工具 [6][8]。

## 术语辨析：$e$ 与欧拉-马歇罗尼常数 $\gamma$

这是本主题最易混淆之处，必须区分两个不同的常数：

- **$e\approx 2.718281828\ldots$**：自然对数的底，本页主题 [1][5][6]。
- **欧拉-马歇罗尼常数 $\gamma\approx 0.5772156649015328606\ldots$**，亦称「欧拉常数」：定义为 $\gamma=\lim_{n\to\infty}\left(H_n-\ln n\right)$，其中 $H_n$ 为调和数；它由欧拉于 1735 年首次定义（当时用字母 $C$），符号 $\gamma$ 由 Mascheroni（1790）首次使用 [11][13][14]。

MathWorld 明确提示 $\gamma$「不要与常数 $e=2.718281\ldots$ 混淆」[11]。MATLAB 文档也区分二者：要求 $e=2.71828\ldots$ 应使用 `exp(1)` 或 `exp(sym(1))`，而 `eulergamma` 表示 $\gamma$ [14]。此外，MATLAB 还提示「Euler's numbers」（欧拉数）在其他语境下可能指 Eulerian numbers 与 Euler polynomials [14]。

来源 [4] 更进一步，认为把 $e$ 称为「欧拉数」并不恰当，并为先前的用法致歉；但该来源未给出详细理由。这与 [1][2][5] 把「欧拉数」作为 $e$ 的通用别名形成措辞上的冲突，读者应按具体语境判断所指。

## 争议、未核实内容与资料缺口

- **命名权与名称正当性**：[4] 对「欧拉数」这一称谓提出异议，但缺乏完整的史学论证；需查证欧拉 1727 年手稿、1736 年《力学》原文及更早的伯努利文献。
- **非主流定义**：来源 [3] 的读者评论提出「$e$ 是完全图 $K_n$ 的路径总数与哈密顿路总数之比」等说法。该说法未出现在任何权威来源中，应视为未经证实的个人观点，不宜纳入正式定义。
- **科普评论的可靠性**：[3] 是个人博客及其评论，其中包含排版错误（如把极限写成 `lim100`、把复利式写成 $e^{t\backslash 100\%}$ 等），其数学细节需回到 [4][5][8][10] 等来源核对。
- **超越性与无理性的证明史缺失**：本次来源只陈述 $e$ 是无理数与超越数 [1][5][6]，未给出证明者与年份（通常与欧拉 1737 年、埃尔米特 1873 年相关），需补充权威文献。
- **高精度计算与算法**：来源未涉及 $e$ 的高精度计算史与算法。
- **历史细节待核实**：莱布尼茨—惠更斯通信的具体日期与信件编号 [5] 尚需核对原始文献；伯努利 1683 年工作的原始出处 [3] 亦为转述。

## 建议补充的来源

1. OEIS A001113（$e$ 的十进制展开），用于核对数值与位数 [5]。
2. 欧拉《Introductio in analysin infinitorum》（1748），用于考察 $e$ 与指数函数的系统性表述。
3. Hermite（1873）关于 $e$ 超越性的原始论文，以及欧拉 1737 年关于 $e$ 无理性的工作。
4. Maor, *e: The Story of a Number*，用于补足命名与发现史。
5. Wolfram MathWorld 的「e」条目与 Wikipedia 英文版「E (mathematical constant)」，用于交叉验证定义等价性与历史细节。
6. 标准微积分教材中关于 $\lim_{n\to\infty}(1+1/n)^n$ 存在性的严格证明，用于替代博客来源 [3]。

## 参考文献

[1] 自然底数，baike.baidu.com  
[2] e (數學常數)，zh.wikipedia.org  
[3] 阮一峰：数学常数 e 的含义，ruanyifeng.com（含读者评论）  
[4] e 是數列 $\left(1+\frac{1}{n}\right)^n$ 的極限，mathsgreat.com  
[5] e (数学常数)，zh.wikipedia.org  
[6] Understanding the Power of Euler's number，wiris.com  
[7] What's so special about Euler's number e?，youtube.com（3Blue1Brown）  
[8] Euler's Number | The Value of e Calculation & Examples，study.com  
[9] What's so special about Euler's number e?，3blue1brown.com  
[10] Euler's number，AoPS Wiki  
[11] Euler-Mascheroni Constant，mathworld.wolfram.com  
[12] 关于欧拉-马歇罗尼常数意义的讨论，facebook.com  
[13] Euler-Mascheroni Constant，Brilliant Math & Science Wiki  
[14] eulergamma，mathworks.com（MATLAB 文档）  
[15] Euler's Gamma Constant，youtube.com

## References

1. [自然底数](https://baike.baidu.com/item/%E8%87%AA%E7%84%B6%E5%BA%95%E6%95%B0/2735968) — baike.baidu.com
2. [e (數學常數) - 維基百科，自由的百科全書](https://zh.wikipedia.org/wiki/E_(%E6%95%B0%E5%AD%A6%E5%B8%B8%E6%95%B0)) — zh.wikipedia.org
3. [数学常数e的含义 - 阮一峰的网络日志](https://www.ruanyifeng.com/blog/2011/07/mathematical_constant_e.html) — ruanyifeng.com
4. [e 是數列n 1 + 1 n o 的極限](http://www.mathsgreat.com/numbers/numbers_005.pdf) — mathsgreat.com
5. [e (数学常数) - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/E_(%E6%95%B0%E5%AD%A6%E5%B8%B8%E6%95%B0)) — zh.wikipedia.org
6. [Understanding the Power of Euler's number](https://www.wiris.com/en/blog/euler-number-properties-uses) — wiris.com
7. [What's so special about Euler's number e?](https://www.youtube.com/watch?v=m2MIpDrF7Es) — youtube.com
8. [Euler's Number | The Value of e Calculation & Examples - Lesson | Study.com](https://study.com/learn/lesson/value-eulers-number-calculation-examples-math.html) — study.com
9. [What's so special about Euler's number e? | 3Blue1Brown](https://www.3blue1brown.com/lessons/eulers-number) — 3blue1brown.com
10. [Euler's number - AoPS Wiki](https://artofproblemsolving.com/wiki/index.php/Euler%27s_number) — artofproblemsolving.com
11. [Euler-Mascheroni Constant -- from Wolfram MathWorld](https://mathworld.wolfram.com/Euler-MascheroniConstant.html) — mathworld.wolfram.com
12. [What is the Euler-Mascheroni constant's significance in ...](https://www.facebook.com/groups/559208084589177/posts/2133341367175833) — facebook.com
13. [Euler-Mascheroni Constant | Brilliant Math & Science Wiki](https://brilliant.org/wiki/euler-mascheroni-constant) — brilliant.org
14. [eulergamma - Euler–Mascheroni constant - MATLAB](https://www.mathworks.com/help/symbolic/sym.eulergamma.html) — mathworks.com
15. [Euler's Gamma Constant](https://www.youtube.com/watch?v=UnA5Ji5XUuA) — youtube.com
