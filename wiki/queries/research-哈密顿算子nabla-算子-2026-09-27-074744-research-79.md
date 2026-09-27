---
type: query
title: "Research: 哈密顿算子（nabla 算子 ∇）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 哈密顿算子（nabla 算子 ∇）

# 哈密顿算子（nabla 算子 ∇）

## 定义

哈密顿算子 ∇（读作 nabla，亦称 del 算子、Atled 算子）是一个**矢量微分算子**：在笛卡儿坐标中，它被定义为沿各坐标轴方向偏导数所组成的"向量"[8][9]：

$$\nabla = \mathbf{i}\,\frac{\partial}{\partial x} + \mathbf{j}\,\frac{\partial}{\partial y} + \mathbf{k}\,\frac{\partial}{\partial z}$$

形式上它是向量，但分量不是数而是微分运算，因此只有在作用于其右侧的对象（标量场或向量场）时才获得意义[1][3]。其最直接的用途是把场论中的三类基本运算统一为"算子作用"的形式[1][3][8][9]：

- 梯度：$\nabla f$（作用于标量场，得向量场）
- 散度：$\nabla\cdot\mathbf{A}$（点乘向量场，得标量场）
- 旋度：$\nabla\times\mathbf{A}$（叉乘向量场，得向量场）
- 拉普拉斯算子：$\nabla\cdot\nabla = \nabla^2 = \Delta$（见 [[拉普拉斯算子]]）

## 术语与历史

nLab 指出，nabla 是"一个古老乐器"——倒三角形——的名字，形状类似亚述竖琴；术语 Atled 与 Del 来自"倒置的大写希腊字母 Δ"，而偏导符号 $\partial$ 有时被视为其小写对应物[9]。nLab 将 ∇ 的历史追溯至 William Hamilton（即引入四元数与哈密顿力学的 Hamilton），并指出 Maxwell 用它书写其方程[9]。

一则物理史普及文章给出了更细的版本[7]：Hamilton 曾把 del 作用于向量 Q，得到"标量结果"与"向量结果"两部分，分别等价于现代的 $\nabla\cdot\mathbf{Q}$ 与其负号形式、以及 $\nabla\times\mathbf{Q}$；但该文作者认为 Hamilton 本人*没有*迈出"把 del 作用于标量"这一步（即现代的梯度）。文中称 Hamilton 于 1847 年创造该算子，最初用倒置的 δ/三角形表示，后改为侧向三角形[7]。该文还强调，正是 Tait 的工作使 Maxwell 注意到这一算子，进而促成 Heaviside 与 Gibbs 建立向量代数；但它也承认 Hamilton / Grassmann / Clifford 之间的历史归属存在大量争论[7]。

标题术语需注意：**Hamilton 算子 / Hamiltonian operator 在向量分析中指的正是 ∇**，但必须与力学意义上的 [[哈密顿算子]]（Hamiltonian）严格区分[6][9]。

## 正交曲线坐标系中的表达式

∇ 及其派生算符（拉普拉斯、梯度、散度、旋度）在不同曲线坐标系中的具体表达式并不相同[2]。设三维正交曲线坐标系 $(u_1,u_2,u_3)$，单位向量为 $\mathbf{e}_1,\mathbf{e}_2,\mathbf{e}_3$，度规因子为 $h_1,h_2,h_3$，则[2][5]：

$$\nabla f = \frac{1}{h_1}\frac{\partial f}{\partial u_1}\mathbf{e}_1 + \frac{1}{h_2}\frac{\partial f}{\partial u_2}\mathbf{e}_2 + \frac{1}{h_3}\frac{\partial f}{\partial u_3}\mathbf{e}_3$$

该式可由方向导数 $\partial f/\partial\nu$ 与 $(3.1),(3.2)$ 式的比较直接得到；作者给出的"真正的理由"是**量纲平衡**——每一项都必须带上 $1/h_i$[5]。同一文献亦逐面元计算了旋度分量，例如

$$\nabla\times\mathbf{A}\big|_{\mathbf{e}_2} = \frac{1}{h_3 h_1}\left(\frac{\partial (A_1h_1)}{\partial u_3} - \frac{\partial (A_3h_3)}{\partial u_1}\right)$$

并以圆柱坐标、球坐标中的梯度与拉普拉斯作为算例，用"计数 $L$ 的量纲"方式校验各项量纲的一致性[5]。

## 运算律与向量恒等式

入门叙述通常强调"梯度作用于标量、散度与旋度作用于向量"[1][3][4]。但严格来说，$\nabla$ **可以作用于向量**：向量的梯度不是向量，而是二阶张量（即 Jacobian 矩阵），它与向量的点乘给出向量[10]。该文以指标记号把这层结构写清楚：

$$\nabla_A(\mathbf{A}\cdot\mathbf{B}) = A^k{}_{,l}B^k\mathbf{e}_l,\qquad (\mathbf{B}\cdot\nabla)\mathbf{A} = B^kA^l{}_{,k}\mathbf{e}_l,\qquad \mathbf{B}(\nabla\cdot\mathbf{A}) = B^lA^k{}_{,k}\mathbf{e}_l$$

并指出这三者恰是 $\mathbf{B}\otimes\nabla\mathbf{A}$ 的三种可能缩并；两个反称"装置"分别是第一与第二、第一与第三式的差，这给出了第四、第五条恒等式的"干巴巴"证明[10]。

另一类重要约束来自坐标对称性：恒等式中的所有算符与运算都必须是坐标对称的，否则表达式在曲线坐标下会失效[1]。

## 与嘉当微分学的关系

《数学指南——实用数学手册》把这一主题放在**1.9 向量分析与物理学领域**，其中包括 1.9.2 梯度、散度和旋度、**1.9.4 哈密顿算子的运算**、1.9.6 对力学守恒律的应用、1.9.9 由源与涡确定向量场、1.9.10 对电磁学中 Maxwell 方程的应用，以及 **1.9.11 经典向量分析与嘉当微分学的关系**[11]。也就是说，∇ 的形式运算在更现代的框架下被 [[嘉当导数与闭包]]、[[微分形式拉回]] 等外微分语言所取代。该节目前尚未入库，构成一处明确的知识缺口（参见下文）。

## 应用

- **电磁学**：Maxwell 用 ∇ 书写其方程[9]；见 [[麦克斯韦方程]]。
- **力学与守恒律**：∇ 用于表述功、势能与守恒律[11]。
- **量子力学**：动能项常写作 $-\frac{\hbar^2}{2m}\nabla^2 + V(q)$，此时 $\nabla^2$ 即拉普拉斯算子（见 [[薛定谔方程]]、[[哈密顿算子]]）[12][13]。
- **偏微分方程**：拉普拉斯方程、热方程、波方程等均可由 ∇ 与 $\nabla^2$ 表出，见 [[偏微分方程]]、[[热方程]]、[[波方程]]、[[调和函数]]。

## 命名歧义：∇ 与量子力学的哈密顿算符 Ĥ

这是本主题最关键的一处**术语冲突**：

- 向量分析/四元数分析中的 "Hamilton 算子 / Hamiltonian operator" 指 **∇**（nabla）[6][9]；
- 力学与量子力学中的 "Hamiltonian" 指系统的哈密顿函数/哈密顿算符 **Ĥ**，即总能量算符，由动能项与势能项构成（[[哈密顿算子]]）[6][13]。

nLab 明确写道，两者是"无关联的（unrelated）"概念，必须在用语上严格区分[6][9]。中文语料中这一区分往往含混：部分百科条目直接以"哈密顿算符"指代量子力学能量算符 Ĥ[13]，而另一些文章以"哈密顿算符"指 ∇[2]。本页采用"哈密顿算子 ∇"表示后者。相关的力学语境可参见 [[哈密顿-雅可比微分方程]]、[[程函方程]]。

## 未决问题与来源缺口

1. **历史归属缺乏一手依据**：[7] 断言"Hamilton 于 1847 年创造了 del 算子"并称此事"无可争议"，但该文为普及性博客，未引 Hamilton 原著（如 *Lectures on Quaternions*）或 Maxwell 的 *Treatise*；[9] 只笼统称 Hamilton 引入、Maxwell 使用。两者在时间线细节上不能互相校验。
2. **符号约定冲突**：[7] 称在 Hamilton 的四元数运算中，"nabla 无向量项、标量结果是该函数（即 $\partial_x^2+\partial_y^2+\partial_z^2$）的负值"，这与现代 $\nabla\cdot\nabla=+\Delta$ 的约定符号相反。该符号差异是四元数约定与现代向量分析约定的差别，还是文本误述，来源未交代。
3. **"梯度不能作用于向量"的常见说法被反驳**：[10] 明确指出该说法"patently false"，向量梯度是二阶张量。这与 [3][4] 等入门叙述的表述口径不一致（后者把 ∇ 限定为三种基本运算）。
4. **曲线坐标系公式的适用条件**：[2][5] 讨论正交曲线坐标，未讨论非正交坐标或一般流形上的协变导数/联络；∇ 在黎曼流形上的推广在本批来源中完全缺席。
5. **《数学指南》1.9 各子节未入库**：[11] 表明 1.9.2、1.9.4、1.9.9、1.9.10、1.9.11 等直接相关小节目前没有对应 wiki 页面，尤其是 1.9.11「经典向量分析与嘉当微分学的关系」。
6. **来源结构失衡**：现有 14 条来源中，博客/专栏/百科类占多数，仅 [6][9]（nLab）与 [5]（《數學傳播》）为较规范的学术性说明；缺少教材级的一手推导。

## 建议补充的来源

- Hamilton, W. R., *Lectures on Quaternions*（1853）——用于核实 del 算子的最初定义与符号。
- Maxwell, J. C., *A Treatise on Electricity and Magnetism*——用于核实 ∇ 在电磁学中的引入。
- Tai, C.-T. 关于向量分析史的系列论文（如 "A historical study of vector analysis"）——用于厘清 Hamilton / Tait / Heaviside / Gibbs / Grassmann 的归属争议[7]。
- 《数学指南——实用数学手册》1.9.2、1.9.4、1.9.9、1.9.11 各节原文[11]——用于补齐 ∇ 的完整运算律与嘉当微分学对应关系。
- 标准教材章节：如 Shilov, *Mathematical Analysis*（多实变量函数部分，nLab 页所引）[9]；以及任何含正交曲线坐标下 grad/div/curl 完整推导的场论教材。

## 相关条目

[[哈密顿算子]]、[[拉普拉斯算子]]、[[麦克斯韦方程]]、[[偏微分方程]]、[[热方程]]、[[波方程]]、[[调和函数]]、[[薛定谔方程]]、[[嘉当导数与闭包]]、[[微分形式拉回]]、[[哈密顿-雅可比微分方程]]、[[程函方程]]、[[庞加莱微分算子]]、[[复可微与复导数]]、[[广义导数]]、[[索伯列夫空间]]

## References

1. [Nabla 算符(∇)](https://zhuanlan.zhihu.com/p/1951332340912587907) — zhuanlan.zhihu.com
2. [哈密顿算符及其一般运算表达式的分析](https://www.hanspub.org/journal/paperinformation?paperid=37173) — hanspub.org
3. [哈密顿算子与梯度、散度、旋度](https://blog.csdn.net/irober/article/details/106231611) — blog.csdn.net
4. [哈密顿算符梯度散度旋度的补充](https://blog.csdn.net/pjm616/article/details/127659438) — blog.csdn.net
5. [數學傳播 | 圖解梯度、散度與旋度](https://www.math.sinica.edu.tw/mathmedia/journals/4386) — math.sinica.edu.tw
6. [Hamiltonian in nLab](https://ncatlab.org/nlab/show/Hamiltonian) — ncatlab.org
7. [Quaternions to Vector Analysis - Kathy Loves Physics](https://kathylovesphysics.com/quaternions-to-vector-analysis) — kathylovesphysics.com
8. [Operator Nabla - an overview | ScienceDirect Topics](https://www.sciencedirect.com/topics/engineering/operator-nabla) — sciencedirect.com
9. [nabla in nLab](https://ncatlab.org/nlab/show/nabla) — ncatlab.org
10. [HELP! A Stubborn Vector Identity to Understand – TensorTime](https://tensortime.sticksandshadows.net/archives/642) — tensortime.sticksandshadows.net
11. [数学指南-实用数学手册_目录德国- redufa](https://www.cnblogs.com/redufa/p/18668710) — cnblogs.com
12. [数学的艺术—— 哈密顿方程](https://zhuanlan.zhihu.com/p/1982400897565876582) — zhuanlan.zhihu.com
13. [哈密顿算符](https://baike.baidu.com/item/%E5%93%88%E5%AF%86%E9%A1%BF%E7%AE%97%E7%AC%A6/9108762) — baike.baidu.com

## Related
- [[queries/research-由-191-展开的经典力学向量分析应用值得追踪-2026-09-27-074904-research-84]]
- [[queries/research-曲线坐标下梯度散度旋度的张量分析一般公式尚缺专页-2026-09-27-074908-research-85]]
