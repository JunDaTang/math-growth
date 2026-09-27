---
type: query
title: "Research: 雅可比行列式（Jacobi 行列式）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 雅可比行列式（Jacobi 行列式）

# 雅可比行列式（Jacobi 行列式）

雅可比行列式是多元微积分中刻画坐标变换局部伸缩与定向的核心工具，它在多重积分的换元法、反函数定理、隐函数定理，以及微分方程稳定性分析等领域都扮演关键角色。本页综合多份中文与外文资料，给出其定义、几何意义、在积分换元中的作用，并记录不同来源在记号与约定上的分歧。

## 定义与记号

在向量分析中，**雅可比矩阵**（Jacobian matrix，也译作 Jacobi 矩阵）是把函数的一阶[[偏导数|偏导数]]按一定方式排列成的矩阵；当该矩阵为方阵时，其行列式称为**雅可比行列式**（Jacobian determinant）[11][15]。需注意，英文中「Jacobian」一词既可指矩阵，也可指行列式，中文资料时常不加区分[6][11]。

对二元变换 $T: x = g(u,v),\ y = h(u,v)$，雅可比行列式定义为 [7][8]：

$$J(u,v)=\frac{\partial(x,y)}{\partial(u,v)}=\begin{vmatrix}\dfrac{\partial x}{\partial u} & \dfrac{\partial x}{\partial v}\\[2mm] \dfrac{\partial y}{\partial u} & \dfrac{\partial y}{\partial v}\end{vmatrix}=\frac{\partial x}{\partial u}\frac{\partial y}{\partial v}-\frac{\partial x}{\partial v}\frac{\partial y}{\partial u}.$$

对三元变换 $T: x=g(u,v,w),\ y=h(u,v,w),\ z=p(u,v,w)$，则是一个 $3\times3$ 行列式 [7][8]：

$$J(u,v,w)=\frac{\partial(x,y,z)}{\partial(u,v,w)}=\begin{vmatrix}\dfrac{\partial x}{\partial u} & \dfrac{\partial x}{\partial v} & \dfrac{\partial x}{\partial w}\\[2mm] \dfrac{\partial y}{\partial u} & \dfrac{\partial y}{\partial v} & \dfrac{\partial y}{\partial w}\\[2mm] \dfrac{\partial z}{\partial u} & \dfrac{\partial z}{\partial v} & \dfrac{\partial z}{\partial w}\end{vmatrix}.$$

一般地，雅可比行列式是以 $n$ 个 $n$ 元函数的偏导数为元素的行列式；在函数均连续可微（偏导数连续）的前提下，它就是函数组的微分形式的一种表述 [15]。

## 几何意义：微元的伸缩因子

雅可比行列式的绝对值是换元前后微元面积的比值 [2]：

$$\mathrm{d}x\,\mathrm{d}y = |J|\,\mathrm{d}u\,\mathrm{d}v.$$

更一般地，$\Delta A \approx J(u,v)\,\Delta u\,\Delta v = \left|\frac{\partial(x,y)}{\partial(u,v)}\right|\Delta u\,\Delta v$ [8]。其几何根据是：$n$ 维体积元 $\mathrm{d}V$ 在新坐标系中一般是一个平行多面体，而平行多面体的 $n$ 维体积正是其各边向量构成的行列式 [6]。因此雅可比行列式充当「缩放因子」，用于修正坐标变换造成的几何畸变，这正是它出现在换元积分中的原因 [10][11]。

由此可推导出一些常用结论，例如极坐标变换 $x = r\cos\theta,\ y = r\sin\theta$ 的雅可比行列式为 $r$，从而 $\mathrm{d}x\mathrm{d}y = r\,\mathrm{d}r\,\mathrm{d}\theta$ [2]。

## 定向（orientation）

雅可比行列式的**符号**携带定向信息：若在点 $p$ 处其值为正，则 $F$ 保持定向（preserves orientation）；若为负，则 $F$ 逆转定向（reverses orientation）；而其绝对值则度量 $F$ 在 $p$ 点附近放大或缩小体积的程度 [11]。

以中文维基百科所举的三维例子为例 [11]：设 $F:\mathbb{R}^3\to\mathbb{R}^3$ 的分量为
$$y_1=5x_2,\quad y_2=4x_1^2-2\sin(x_2x_3),\quad y_3=x_2x_3,$$
其雅可比行列式为
$$\begin{vmatrix}0 & 5 & 0\\ 8x_1 & -2x_3\cos(x_2x_3) & -2x_2\cos(x_2x_3)\\ 0 & x_3 & x_2\end{vmatrix}=-40x_1x_2.$$
可见当 $x_1$ 与 $x_2$ 同号时 $F$ 逆转定向；该函数除 $x_1=0$ 或 $x_2=0$ 的点外处处具有反函数 [11]。

## 在多重积分换元中的作用

雅可比行列式最基本的用途是多重积分的变量替换。设变换 $T: x=g(u,v),\ y=h(u,v)$ 把 $uv$ 平面上的闭有界区域 $S$ 映到 $xy$ 平面上的区域 $R$，并假设 $T$ 在 $S$ 内部为一一映射、$g,h$ 具有连续一阶偏导数。若 $f$ 在 $R$ 上连续，则 [7]：

$$\iint_R f(x,y)\,\mathrm{d}A=\iint_S f\big(g(u,v),\,h(u,v)\big)\,|J(u,v)|\,\mathrm{d}A.$$

注意积分公式中使用的是 $|J|$（绝对值），以抵消定向符号的影响。三重积分的换元法则在两变量情形的基础上完全类似 [7]。这一换元思想与一元积分的[[代换公式|代换公式]]（换元积分法）一脉相承，只是需要额外考虑多个变量之间的相互关系 [4]，并通过雅可比行列式反映新旧坐标系之间的比例关系 [4]。

## 与其他概念的关系

雅可比矩阵是单变量实函数[[全微分|微分]]在向量值多变量函数上的推广，代表函数在给定点的最佳线性逼近，因此在这个意义上也可称作函数在点 $x$ 的微分或导数 [11]。由此：

- **反函数定理**：连续可微函数 $F$ 在点 $p$ 的雅可比行列式不等于零，是 $F$ 在 $p$ 附近存在可微反函数的充要条件 [6][11]。这正是 [[反函数求导法则|反函数求导法则]] 在多变量情形的推广——非零性由导数的非零替换为雅可比行列式的非零，导数的倒数替换为雅可比矩阵的逆 [6]。
- **隐函数定理**：同样可由雅可比行列式的非零性表述 [6]。
- **全局可逆性**：与雅可比行列式处处非零相关的全局问题即著名的雅可比猜想（Jacobian conjecture）[6]。
- **微分方程稳定性**：雅可比矩阵可用于判断微分方程平衡点的稳定性，方法是近似平衡点附近的行为 [6]。

## 应用场景

- **多重积分换元**：二重、三重积分的坐标变换（如极坐标、柱坐标、球坐标）[1][2][3][7]。
- **反函数定理与隐函数定理**：作为定理成立条件的核心量 [6]。
- **微分方程平衡点的稳定性分析** [6]。
- **代数几何**：代数曲线的雅可比行列式对应**雅可比簇**（Jacobian variety），即伴随该曲线的一个代数群，曲线可嵌入其中 [11]。
- **计算机图形学/数值模拟**：例如在 FFT 海面模拟中用于求浪尖泡沫区域 [5]。
- **计算工具中的实现**：如 PTC 的 Mathcad 提供「使用雅可比行列式」的任务流程，步骤包括定义被积函数、在区域内积分、用 $u,v$ 定义 $x,y$、定义向量函数 $F(u,v)$、计算雅可比矩阵，再求其行列式 [13]。

## 历史与命名

雅可比行列式以普鲁士数学家**卡尔·古斯塔夫·雅各布·雅可比**（Carl Gustav Jacob Jacobi, 1804—1851）命名 [7][11]。

## 记号约定上的分歧（重要）

不同来源在以下两点上存在显著差异，阅读时须留意：

1. **矩阵的行列排列方式**：CSUN 教材 [7] 把 $\partial(x,y)/\partial(u,v)$ 写成
   $\begin{vmatrix}\partial x/\partial u & \partial x/\partial v\\ \partial y/\partial u & \partial y/\partial v\end{vmatrix}$，
   即以「旧坐标」为行、「新坐标」为列；而 LibreTexts [8] 则写成
   $\begin{vmatrix}\partial x/\partial u & \partial y/\partial u\\ \partial x/\partial v & \partial y/\partial v\end{vmatrix}$，
   即互为转置。两者行列式数值相同（因为 $\det M = \det M^{\mathsf T}$），但矩阵本身不同。
2. **「Jacobian」所指对象**：有的书把雅可比矩阵本身称为 Jacobian，有的书（如 [7]）则把偏导数矩阵的行列式称为 Jacobian [7][11]。
3. **是否取绝对值**：几何比值与面积元关系写作 $|J|$ [2]，但换元的定理陈述中往往显式写出 $|J(u,v)|$ [7]，而某些教材的记号 $J(u,v)$ 已隐含取绝对值 [8]。

这些差异并非内容矛盾，而是约定不同，但会直接影响公式的书写形式，因此在引用与教学时需明确所选约定。

## 与既有知识体系的关联

本页概念与手册相关的积分、微分主题紧密相连：多元积分的换元建立在 [[多变量函数的积分|多变量函数的积分]] 之上，其线性性来自 [[积分的线性性|积分的线性性]]；矩阵元素的来源是 [[偏导数|偏导数]] 与 [[全微分|全微分]]，其组合规则可对照 [[多变量链式法则|多变量链式法则（表 0.38）]]；一元特例则回到 [[代换公式|代换公式]] 与 [[牛顿-莱布尼茨积分基本定理|牛顿-莱布尼茨积分基本定理]]。手册中的 [[一阶导数表|一阶导数表（表 0.35）]]、[[高阶导数表|高阶导数表（表 0.36）]] 提供了构建雅可比矩阵所需的各基本函数偏导数。

## 存疑与待补充

- **手册中的对应节**：现有资料未指向《[[数学指南实用数学手册|数学指南——实用数学手册]]》中专门论述雅可比行列式或多元换元的章节，其具体表号与公式形式尚待核对。
- **收敛条件与正则性**：换元定理中「一一映射」「连续偏导」等条件在不同教材中的强弱表述略有出入 [7][8]，需对照严格分析教材确认。
- **雅可比猜想**：本页仅提及，未展开；其陈述与已知结果（如各维情形的可证性）值得单独查明 [6]。
- **球坐标与柱坐标的雅可比**：来源仅明确给出极坐标例子 [2]，其他常见坐标系之行列式值宜补充。
- **定向与带符号积分**：绝对值与实际定向积分的关系未在现有来源中给出严谨讨论。
- **来源重复**：[8] 与 [9] 内容相同、[11] 与 [12] 为同一中文维基条目之简繁体版本，引用时可视为单一来源。

## 建议补充的来源

- 严谨分析教材中「反函数定理」「隐函数定理」「变量替换定理」的完整陈述与证明。
- 关于雅可比猜想（Jacobian conjecture）的综述。
- 手册中若存在多元换元或雅可比行列式的专门小节，应补录并交叉核对记号。
- 代数几何中「雅可比簇」的入门材料，以补全命名同源的另一含义。

## 参考文献

[1] 二重积分和雅可比行列式（CSDN）  
[2] 超强换元法，二重积分计算的核武器！（雅可比行列式超通俗讲解，知乎）  
[3] 多重积分（百度百科）  
[4] 雅可比行列式（cnblogs）  
[5] （完全理解）二重积分中的换元积分中的雅可比矩阵（CSDN）  
[6] Jacobian matrix and determinant, Wikipedia (en)  
[7] 16.7 Change of Variables in Multiple Integrals (CSUN)  
[8] 14.7 Change of Variables in Multiple Integrals (Jacobians), Mathematics LibreTexts  
[9] 14.7 Change of Variables in Multiple Integrals (Jacobians), Mathematics LibreTexts（与 [8] 重复）  
[10] Change of Variables in Multiple Integrals, StudySmarter  
[11] 雅可比矩阵（维基百科，简体）  
[12] 雅可比矩阵（维基百科，繁体，与 [11] 同源）  
[13] 任务 3-5：使用雅可比行列式（PTC Support）  
[14] 雅可比矩阵和雅可比行列式（知乎）  
[15] 雅可比行列式（百度百科）

## References

1. [二重积分和雅可比行列式](https://blog.csdn.net/xiaoyink/article/details/88432372) — blog.csdn.net
2. [超强换元法，二重积分计算的核武器！（雅可比行列式超通俗 ...](https://zhuanlan.zhihu.com/p/382301310) — zhuanlan.zhihu.com
3. [多重积分](https://baike.baidu.com/item/%E5%A4%9A%E9%87%8D%E7%A7%AF%E5%88%86/8496562) — baike.baidu.com
4. [雅可比行列式](https://www.cnblogs.com/2002cjc/p/18276185) — cnblogs.com
5. [（完全理解）二重积分中的换元积分中的雅可比矩阵原创](https://blog.csdn.net/qq_43391414/article/details/127758298) — blog.csdn.net
6. [Jacobian matrix and determinant - Wikipedia](https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant) — en.wikipedia.org
7. [16.7 Change of Variables in Multiple Integrals](http://www.csun.edu/~hcmth008/250/bccalclt03_1607.pdf) — csun.edu
8. [14.7: Change of Variables in Multiple Integrals (Jacobians) - Mathematics LibreTexts](https://math.libretexts.org/Courses/Monroe_Community_College/MTH_212_Calculus_III/Chapter_14:_Multiple_Integration/14.7:_Change_of_Variables_in_Multiple_Integrals_(Jacobians)) — math.libretexts.org
9. [14.7: Change of Variables in Multiple Integrals (Jacobians) - Mathematics LibreTexts](https://math.libretexts.org/Courses/Monroe_Community_College/MTH_212_Calculus_III/Chapter_14%3A_Multiple_Integration/14.7%3A_Change_of_Variables_in_Multiple_Integrals_(Jacobians)) — math.libretexts.org
10. [Change of Variables in Multiple Integrals](https://www.studysmarter.co.uk/explanations/math/calculus/change-of-variables-in-multiple-integrals) — studysmarter.co.uk
11. [雅可比矩阵 - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/%E9%9B%85%E5%8F%AF%E6%AF%94%E7%9F%A9%E9%98%B5) — zh.wikipedia.org
12. [雅可比矩阵 - 维基百科，自由的百科全书](https://zh.wikipedia.org/wiki/%E9%9B%85%E5%8F%AF%E6%AF%94%E7%9F%A9%E9%98%B5) — zh.wikipedia.org
13. [任务3-5：使用雅可比行列式](https://support.ptc.com/help/mathcad/r11.0/zh_CN/PTC_Mathcad_Help/Tutorials/slv_tutorial/task3-5_working_with_the_jacobian.html) — support.ptc.com
14. [雅可比矩阵和雅可比行列式](https://zhuanlan.zhihu.com/p/443813176) — zhuanlan.zhihu.com
15. [雅可比行列式](https://baike.baidu.com/item/%E9%9B%85%E5%8F%AF%E6%AF%94%E8%A1%8C%E5%88%97%E5%BC%8F/4709261) — baike.baidu.com

## Related
- [[queries/research-152-节与-15104-例-11-尚未入库-2026-09-27-074536-research-70]]
