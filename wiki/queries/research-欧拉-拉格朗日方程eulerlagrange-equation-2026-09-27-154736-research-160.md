---
type: query
title: "Research: 欧拉-拉格朗日方程（Euler–Lagrange equation）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 欧拉-拉格朗日方程（Euler–Lagrange equation）

# 欧拉-拉格朗日方程（Euler–Lagrange equation）

## 概述与定位

欧拉-拉格朗日方程（Euler–Lagrange equation）是**变分法（calculus of variations）**与**经典力学（classical mechanics）**中的核心方程。[1][6] 它给出泛函取平稳值（stationary value，即临界值）的必要条件：其解正是使给定**作用量泛函（action functional）**达到驻点（stationary point）的函数。[1][5][6] 这类问题的求解统称为变分法。[5]

从数学对象上看，欧拉-拉格朗日方程是一组**二阶常微分方程（ordinary differential equations, ODE）**，方程的解对应泛函的驻点。[1] 在变分法语境下，这一方程常被简称为"Lagrange 方程"（Lagrange equations）。[1] Wolfram MathWorld 将其称为"变分法的基本方程"（the fundamental equation of calculus of variations）。[3]

其直观来源可追溯到初等微积分中"可导函数在极值点导数为零"这一基本事实的推广：[8] 正如令一元函数的一阶导数为零可求得极值点，令泛函的**变分（variation）**为零即可求得驻点函数。

## 数学表述

设泛函 $J$ 由如下形式的积分定义：[3]

$$J[y] = \int_a^b L\big(x,\, y(x),\, y'(x)\big)\, \mathrm{d}x$$

其中被积函数 $L$ 称为 **Lagrangian（拉格朗日量 / 拉格朗日函数）**。$J$ 取平稳值的必要条件是 $y$ 满足欧拉-拉格朗日方程：

$$\frac{\partial L}{\partial y} - \frac{\mathrm{d}}{\mathrm{d}x}\!\left(\frac{\partial L}{\partial y'}\right) = 0$$

这一形式即所谓的"第一方程"；在此之外，中文维基百科的条目还列出了"第二方程"及若干例子。[6] 一个经典算例是"两点之间最短曲线"的求解。[6]

在**多个因变量**或**场**的情形，方程推广为每个分量各对应一个方程；在经典力学中即每个广义坐标对应一个欧拉-拉格朗日方程（见下节）。

## 推导思路

欧拉-拉格朗日方程的推导以变分法为基础。[2][7][15] 基本思路是：对候选函数 $y(x)$ 施加微小扰动 $y + \varepsilon\eta$，考察泛函 $J$ 的一阶变分 $\delta J$ 并为零，再对含 $\eta'$ 的项作**分部积分**，最后利用变分法的基本引理（函数的任意变分下积分恒为零意味着被积函数为零）得到上述方程。[2][7]

Euler 本人的原始方法更为初等：他把待求曲线用一条**小折线（多边形）**逼近，对多边形的顶点坐标求极值，再令分点数目趋于无穷，从而把离散的极值问题过渡到连续的变分问题。[8] 这一"由折线逼近曲线"的思想，正是把初等微积分极值理论推广至泛函的历史路径。[8]

## 在经典力学中的形式

在经典力学中，欧拉-拉格朗日方程给出系统的运动方程。[10] 此时 Lagrangian 定义为**动能减势能**：[9][10]

$$L = T - V$$

其中 $T$ 是系统的动能（kinetic energy），$V$ 是势能（potential energy）。[9][10] 对单质点，$T = \tfrac{1}{2} m (\dot{X} \cdot \dot{X})$。[9] 以**广义坐标** $q$ 与**广义速度** $\dot{q}$ 表示，运动方程为：

$$\frac{\partial L}{\partial q_i} - \frac{\mathrm{d}}{\mathrm{d}t}\!\left(\frac{\partial L}{\partial \dot{q}_i}\right) = 0$$

值得注意的是，势能 $V$ 通常不显含 $\dot{q}$，但在讨论某些推广情形时需加以留意。[10] 在力学语境下，该方程可由**虚功原理**（结合 d'Alembert 原理）导出。[9]

## 历史脉络与命名

关于方程的命名与发现优先权，存在一段值得注意的历史：

- **1743 年 4 月 15 日之前**，Euler 已发现了今天被称为欧拉-拉格朗日方程的结果——这是根据 Goldstine 的记述。[12]
- **1744 年**，Euler 的著作 *Methodus inveniendi* 出版，[11] 该书把一系列特殊情形转化为对一般问题的系统化处理，标志着变分法的诞生。[14]
- **1755 年**，Lagrange 在致 Euler 的信中提出了新的处理方法，使变分法的发展出现新的转折。[11] Lagrange 的新"变分法"的核心，在于为"关于曲线上的积分表达式"定义一种新的导数 / 微分概念。[4]
- 尽管发现优先权归于 Euler，但由于 Lagrange 的解析方法影响深远，今日通行的名称把两者并列，称为 **Euler–Lagrange equation**；在不同语境中，它也常被径直称为 **Lagrange 方程**。[1]

（Euler 1744 年著作与 Lagrange 1755 年方法的具体年份在不同来源间的表述见 [11][12]，亦可参见下节的矛盾说明。）

## 相关理论与延伸

- **哈密顿原理 / 最小作用量原理**：欧拉-拉格朗日方程是该原理的数学表述形式。
- **Weierstrass 与变分法的严格化**：变分法的严格性在 19 世纪由 [[魏尔斯特拉斯]] 等人的工作而完善（如 Weierstrass 关于判别极大极小的"多余函数"理论、角点条件等）。多数现代教科书将欧拉-拉格朗日方程视为局部极值必要条件，而充分条件需借助更高阶的判别手段。
- **量子力学中的路径积分**：[[费恩曼]] 的路径积分表述把经典作用量与量子振幅联系起来，可视为变分原理与作用量的进一步推广；这与 [[量子过程的随机性]] 等问题相关。
- **几何与广义相对论**：测地线方程是欧拉-拉格朗日方程的特例，与 [[爱因斯坦]] 的广义相对论中质点沿测地线运动的思想相连。

## 矛盾、疑点与空白

1. **方程类型的分歧：ODE 还是 PDE？** 英文维基百科明确指出欧拉-拉格朗日方程是一组**二阶常微分方程（ODE）**。[1] 而中文维基百科的相应表述称其为"一个**二阶偏微分方程**"。[6] 对于含单个自变量 $x$ 的基本情形，方程应为 ODE；只有当泛函依赖多个自变量（如场论中的多元情形）时才会出现 PDE 形式。两处表述的差异可能是术语使用范围不同所致，需核对条目原文的上下文。

2. **命名优先权与年份的表述差异**：来源 [12] 指出 Euler 的发现早于 1743 年 4 月；来源 [11] 强调 1744 年 *Methodus inveniendi* 的出版与 1755 年 Lagrange 的贡献。不同来源对"谁最先提出"与关键年份的强调不一，宜并列呈现而非择一。

3. **推导细节在本批来源中不完整**：本批资料多为概览性描述或视频标题，缺少从变分 $\delta J = 0$ 到最终方程的完整逐步推演；[2][7][15] 提供了推导的教学性说明，但具体中间步骤未被完整摘录。

4. **特殊情形的公式（如 $L$ 不显含 $x$ 时的 Beltrami 恒等式 / 初积分）** 在来源中未给出，中文维基条目所提到的"第一方程""第二方程"具体指代何种形式，尚待核实。[6]

## 建议补充的来源

- 变分法或经典力学标准教材（如 Goldstein, *Classical Mechanics*；Gelfand & Fomin, *Calculus of Variations*），用于补齐推导与充分条件。
- 关于命名历史的原始文献考证：Euler 的 *Methodus inveniendi*（1744）与 Lagrange 1755 年致 Euler 的信件。
- 关于 Weierstrass 角点条件（Weierstrass–Erdmann conditions）与多余函数的资料，以支持"相关理论与延伸"一节。
- 关于路径积分与最小作用量原理的现代综述，用于连接 [[费恩曼]] 的工作。

## References

1. [Euler–Lagrange equation - Wikipedia](https://en.wikipedia.org/wiki/Euler%E2%80%93Lagrange_equation) — en.wikipedia.org
2. [Derivation of the Euler-Lagrange Equation | Calculus of Variations](https://www.youtube.com/watch?v=sFqp2lCEvwM) — youtube.com
3. [Euler-Lagrange Differential Equation -- from Wolfram MathWorld](https://mathworld.wolfram.com/Euler-LagrangeDifferentialEquation.html) — mathworld.wolfram.com
4. [Lagrange and the calculus of variations | Lettera Matematica](https://link.springer.com/article/10.1007/s40329-014-0049-x) — link.springer.com
5. [The Euler–Lagrange Equation - Gregory Gundersen](https://gregorygundersen.com/blog/2020/05/10/euler-lagrange/) — gregorygundersen.com
6. [欧拉-拉格朗日方程 - 维基百科](https://zh.wikipedia.org/zh-hans/%E6%AD%90%E6%8B%89-%E6%8B%89%E6%A0%BC%E6%9C%97%E6%97%A5%E6%96%B9%E7%A8%8B) — zh.wikipedia.org
7. [Euler-Lagrange Equation (欧拉-拉格朗日方程)推导 - 知乎专栏](https://zhuanlan.zhihu.com/p/148949128) — zhuanlan.zhihu.com
8. [寻找“最好”（2）——欧拉-拉格朗日方程 - 博客园](https://www.cnblogs.com/bigmonkey/p/9519387.html) — cnblogs.com
9. [數學傳播| 虛功原理及歐拉-拉格朗日方程式](https://www.math.sinica.edu.tw/mathmedia/journals/4680?keywords%5B%5D=Euler) — math.sinica.edu.tw
10. [欧拉—拉格朗日方程（经典力学） - 小时百科](https://wuli.wiki/online/Lagrng.html) — wuli.wiki
11. [Who came up with the Euler-Lagrange equation?](https://mathoverflow.net/questions/103623/who-came-up-with-the-euler-lagrange-equation) — mathoverflow.net
12. [Who came up with the Euler-Lagrange equation first?](https://math.stackexchange.com/questions/177243/who-came-up-with-the-euler-lagrange-equation-first) — math.stackexchange.com
14. [Frugal nature: Euler and the calculus of variations | plus.maths.org](https://plus.maths.org/frugal-nature-euler-and-calculus-variations) — plus.maths.org
15. [Introduction to Variational Calculus - Deriving the Euler-Lagrange Equation](https://www.youtube.com/watch?v=VCHFCXgYdvY) — youtube.com

## Related
- [[queries/research-变分问题一般提法-2026-09-27-161005-research-45]]
- [[queries/research-隐约束与非完整约束术语的对应关系-2026-09-27-155528-research-172]]
- [[queries/research-经典变分问题最速降线等周问题测地线作为应用子节的对照证据-2026-09-27-154852-research-161]]
- [[queries/research-是否继续录入-511518-子节以提取实质内容-2026-09-27-154701-research-158]]
- [[queries/research-二阶变分与雅可比方程的联系缺少专页-2026-09-27-155341-research-169]]
