---
type: query
title: "Research: 高斯分布（Gaussian distribution）"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 高斯分布（Gaussian distribution）

# 高斯分布（Gaussian distribution）

## 概述

高斯分布（Gaussian distribution），在统计学中通常称为**正态分布（normal distribution）**，是最基本的连续概率分布之一。其概率密度函数（probability density function, PDF）呈钟形，由两个参数——均值 $\mu$ 与标准差 $\sigma$——完全刻画：

$$P(x)=\frac{1}{\sqrt{2\pi}\,\sigma}\,e^{-\frac{1}{2\sigma^{2}}(x-\mu)^{2}}$$

本页综合多份来源，梳理高斯分布的推导路径：从基础的**高斯积分**（Gaussian integral）的计算技巧，到归一化常数的确定，再到方差参数与指数系数的对应关系，最后延伸至多维推广与应用。相关人物 [[高斯]] 与 [[泊松]] 在推导史上扮演了关键角色。

## 历史渊源

关于高斯分布与高斯积分的归属，来源之间存在值得注意的张力：

- Abraham de Moivre 于 1733 年最早发现这一类型的积分；[[高斯]] 于 1809 年发表了精确的积分结果，并把这一发现归功于 Laplace [11]。
- 因此，尽管该积分以高斯命名，其最早发现权实际属于 de Moivre [11]。这一命名史实提示，"高斯积分"与"高斯分布"的命名更多源于高斯在天文误差分析中的推广作用，而非首创 [11]。
- 最广泛流传的极坐标证明归于 Poisson [5]。Keith Conrad 明确指出，这一极坐标方法是公认最著名的证明，出自 Poisson [5]。

## 高斯积分（Gaussian integral）

### 基本公式

推导高斯分布的核心工具是**高斯积分**。其标准形式为 [1]：

$$\int_{-\infty}^{+\infty} e^{-x^{2}}\,\mathrm{d}x = \sqrt{\pi}, \qquad \int_{-\infty}^{+\infty} e^{-a^{2}x^{2}}\,\mathrm{d}x = \frac{\sqrt{\pi}}{a}$$

该积分在有限积分限的情形下，与**误差函数（error function）**及正态分布的**累积分布函数（cumulative distribution function）**密切相关 [10][11]。它同时也是计算正态分布归一化常数的直接依据 [11]。

### 极坐标证明（Poisson）

最广为人知的证明由 Poisson 给出 [5]，要点是先计算半边积分的平方，再在极坐标下求值。

令 $J=\int_{0}^{\infty}e^{-x^{2}}\,\mathrm{d}x$，则

$$J^{2}=\int_{0}^{\infty}\int_{0}^{\infty} e^{-(x^{2}+y^{2})}\,\mathrm{d}x\,\mathrm{d}y$$

该二重积分的区域为第一象限，在极坐标下为 $\{(r,\theta): r\ge 0,\ 0\le\theta\le\pi/2\}$。将 $x^{2}+y^{2}$ 写为 $r^{2}$，将 $\mathrm{d}x\,\mathrm{d}y$ 写为 $r\,\mathrm{d}r\,\mathrm{d}\theta$，得到 [5]：

$$J^{2}=\int_{0}^{\pi/2}\int_{0}^{\infty} e^{-r^{2}} r\,\mathrm{d}r\,\mathrm{d}\theta = \frac{1}{2}\cdot\frac{\pi}{2}=\frac{\pi}{4}$$

由于 $J>0$，故 $J=\sqrt{\pi}/2$，进而 $I=\int_{-\infty}^{\infty}e^{-x^{2}}\,\mathrm{d}x=\sqrt{\pi}$ [5]。来源 [2][3][6][10] 均复述了将直角坐标与极坐标下的同一积分相等同的思路；其中 [8] 特别强调了极坐标变换中**雅可比行列式（Jacobian）** $|J|=r$ 的引入。

Conrad 同时指出，有论证认为这一方法"不能用于任何其他积分" [5]，这提示该证明技巧的适用范围有限，是一处值得留意的细节。

### 其他证明路径

Keith Conrad 整理了多种证明 [5]，除上述极坐标法外还包括：

1. **另一变量代换**：在内部积分中令 $x=yt$（固定 $y$），将 $J^{2}$ 化为 $\int_{0}^{\infty}\left(\int_{0}^{\infty} y e^{-y^{2}(t^{2}+1)}\,\mathrm{d}y\right)\mathrm{d}t$，其中积分次序的交换由 Fubini 定理保证 [5]。
2. **积分号下求导（Leibniz 法则）**：定义辅助函数并对其求导，利用 $A'(t)=-B'(t)$ 得到关于 $t$ 的恒等式，再通过取极限 $t\to 0^{+}$ 与 $t\to\infty$ 定出常数 $C=\pi/4$，最终仍得 $J^{2}=\pi/4$ [5]。

### 复数形式

在高斯积分的复数形式中，有 [11]：

$$\int_{-\infty}^{\infty} e^{\frac{1}{2}it^{2}}\,\mathrm{d}t = e^{i\pi/4}\sqrt{2\pi}$$

更一般地，对 $\mathbb{R}^{N}$ 有 $\int_{\mathbb{R}^{N}} e^{\frac{1}{2}i x^{T}Ax}\,\mathrm{d}x = \det(A)^{-\frac{1}{2}}\left(e^{i\pi/4}\sqrt{2\pi}\right)^{N}$ [11]。这类结果与 [[复数]] 及复指数运算相关。

## 从高斯积分推导正态分布

### 归一化常数的确定

推导思路是：先假定分布具有对称的指数形式，再用归一化条件与方差条件定出两个待定参数。来源 [4] 给出了一条清晰的路径。

假定 $P(x)=A e^{-kx^{2}}$，由归一化条件 $\int_{-\infty}^{\infty} P(x)\,\mathrm{d}x=1$ 有 $A\int_{-\infty}^{\infty}e^{-kx^{2}}\,\mathrm{d}x=1$ [4]。由于被积函数关于 $x$ 对称，且 $x,y$ 相互独立，可平方后写成二重积分 [4]：

$$A\sqrt{\int_{-\infty}^{\infty}\int_{-\infty}^{\infty} e^{-k(x^{2}+y^{2})}\,\mathrm{d}x\,\mathrm{d}y}=1$$

在极坐标下（利用雅可比 $|J|=r$）[4]：

$$A\sqrt{\int_{0}^{2\pi}\int_{0}^{\infty} e^{-kr^{2}}|J|\,\mathrm{d}r\,\mathrm{d}\theta}=1$$

由此得到 $A=\sqrt{k/\pi}$，即 $P(x)=\sqrt{k/\pi}\,e^{-kx^{2}}$ [4]。

### 方差与指数系数的关系

接下来用方差条件 $\int_{-\infty}^{\infty}x^{2}P(x)\,\mathrm{d}x=\sigma^{2}$ 定出 $k$ [4]：

$$\frac{k}{\pi}\int_{-\infty}^{\infty}x^{2}e^{-kx^{2}}\,\mathrm{d}x=\sigma^{2}$$

来源 [4] 采用**分部积分** $\int_{a}^{b}u\,\mathrm{d}v=uv|_{a}^{b}-\int_{a}^{b}v\,\mathrm{d}u$（取 $u=x$，$\mathrm{d}v=xe^{-kx^{2}}\,\mathrm{d}x$）来求值，最终得到 $k=\dfrac{1}{2\sigma^{2}}$。代回即得标准正态密度 $P(x)=\dfrac{1}{\sqrt{2\pi}\,\sigma}e^{-\frac{x^{2}}{2\sigma^{2}}}$ [4]。

来源 [1] 以另一种参数化 $h$ 完成同一目标：令 $P(\varepsilon)=\dfrac{h}{\sqrt{\pi}}e^{-h^{2}\varepsilon^{2}}$，由 $\mathbb{E}[\varepsilon^{2}]=\sigma^{2}$ 出发，同样使用分部积分（并利用高斯积分 $\int_{0}^{\infty}e^{-h^{2}x^{2}}\mathrm{d}x=\frac{\sqrt{\pi}}{2h}$）[1]，得到 $\sigma^{2}=\dfrac{1}{2h^{2}}$，即 $h=\dfrac{1}{\sigma\sqrt{2}}$。这表明参数 $h$ 与标准差 $\sigma$ 互为倒数关系，两种参数化在数学上等价。

来源 [6] 指出，任何高斯分布只需经线性变换即可化为标准高斯分布，因此只需推导标准形式的积分即可。来源 [4] 最终写出含均值的一般形式：

$$P(x)=\frac{1}{\sqrt{2\pi}\,\sigma}e^{-\frac{1}{2\sigma^{2}}(x-\mu)^{2}}$$

## 高维推广与相关积分

高斯积分的一个关键推广是多变量的二次型积分 [11]：

$$\int_{\mathbb{R}^{n}}\exp\left(-\tfrac{1}{2}\mathbf{x}^{\mathsf T}A\mathbf{x}+\mathbf{b}^{\mathsf T}\mathbf{x}+c\right)\mathrm{d}^{n}\mathbf{x}=\sqrt{\det\left(2\pi A^{-1}\right)}\exp\left(\tfrac{1}{2}\mathbf{b}^{\mathsf T}A^{-1}\mathbf{b}+c\right)$$

该结果被应用于**多维正态分布（multivariate normal distribution）**的研究 [11]。此外还有含高阶矩的积分恒等式，涉及对 $A^{-1}$ 元素指标求和的形式 [11]。这些高维结果对于计算与正态分布相关的连续分布的期望（例如对数正态分布）很有用 [11]。

## 应用

高斯积分与高斯分布在多个学科中频繁出现 [11][12][14]：

- **概率与统计**：确定正态分布的归一化常数，定义误差函数与累积分布函数 [11][13]。
- **量子力学**：用于求谐振子基态的概率密度；在**路径积分（path integral）**表述中用于求谐振子的传播子（propagator）[11]。这与 [[零点能]]、[[薛定谔方程]] 等主题相关。
- **统计力学**：用于配分函数与相关量的计算 [11][12]。
- **傅里叶分析**：高斯函数的傅里叶变换仍为高斯函数 [13][14]。

由于高斯核是扩散过程的解，这一结构也与 [[热方程]] 所刻画的情形形式相通。

## 争议、矛盾与缺口

综合各来源，需要指出以下几点：

1. **命名归属的张力**：高斯积分的首个发现者实为 de Moivre（1733），高斯（1809）只是发表了精确结果并将其归于 Laplace [11]。因此以"高斯"冠名带有历史偶然性。
2. **来源权威性不均**：来源 [12]（facebook）、[14]（linkedin）、[13]（scribd）属于社交媒体或分享平台，内容多为重复性、概述性的常识陈述，权威性较低，仅可作为交叉印证，不宜作为主要依据。相对而言，[5]（Keith Conrad）与 [11]（Wikipedia 英文版）在证明与文献引用上最为严谨。
3. **"高斯如何导出正态分布"的史料不足**：来源 [1] 标题为 "How Did Gauss Derive The Normal Distribution"，但其实际内容集中在积分技巧上，并未给出高斯本人从天文观测误差推导正态分布的历史细节。高斯推导的原始动机与最小二乘法的联系在现有来源中缺位。
4. **极坐标证明的适用性限制**：来源 [5] 提到有观点认为极坐标法"不能用于其他积分"，但未给出充分的论证说明，这一断言的范围与条件有待核实。
5. **变换细节表述不严谨**：来源 [4] 在从 $\int\int e^{-kx^{2}}e^{-ky^{2}}\,\mathrm{d}x\,\mathrm{d}y$ 过渡到 $e^{-k(x+y)^{2}}$ 的书写上出现了明显的笔误（应为 $e^{-k(x^{2}+y^{2})}$），阅读时需注意。

## 建议补充来源

为补足上述缺口，建议查找以下类型的资料：

1. **统计史专著**：如 Stephen Stigler《The History of Statistics》，用于核实正态分布/误差定律的历史脉络与 de Moivre、Laplace、Gauss 三者的实际贡献顺序。
2. **原始文献**：Gauss 1809 年的《Theoria motus corporum coelestium》以及 Laplace 的相关工作，用于还原正态分布的原始推导动机。
3. **严格教材**：关于多维正态分布、路径积分中高斯积分严格处理的数学物理教材，以补足 [11] 中高维公式的推导细节。
4. **误差函数专页**：erf 与正态累积分布函数的定义式、近似与数值表，目前仅被零散提及。
5. **复分析与傅里叶变换**：高斯函数在傅里叶变换下自守性质的严格证明；可对照 [[希尔伯特空间]] 与 [[球面函数]] 等既有条目建立联系。

## References

1. [How Did Gauss Derive The Normal Distribution](https://notarocketscientist.xyz/posts/2023-01-27-how-gauss-derived-the-normal-distribution) — notarocketscientist.xyz
2. [Proof: Gaussian integral](https://statproofbook.github.io/P/norm-gi.html) — statproofbook.github.io
3. [prove Gaussian integral using polar coordinates](https://math.stackexchange.com/questions/1304640/prove-gaussian-integral-using-polar-coordinates) — math.stackexchange.com
4. [Deriving Gaussian Distribution – Ardian Umam blog](https://ardianumam.wordpress.com/2017/10/19/deriving-gaussian-distribution) — ardianumam.wordpress.com
5. [THE GAUSSIAN INTEGRAL Let I = ∫ ∞ e dx, J = ∫ ∞ e ... - Keith Conrad](https://kconrad.math.uconn.edu/blurbs/analysis/gaussianintegral.pdf) — kconrad.math.uconn.edu
6. [高斯分布概率密度函数积分推导](https://www.cnblogs.com/shenchuguimo/p/9843034.html) — cnblogs.com
8. [高斯分布推导极坐标积分公式雅可比矩阵](https://www.zybuluo.com/zsh-o/note/1071280) — zybuluo.com
10. [高斯积分- 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-hans/%E9%AB%98%E6%96%AF%E7%A7%AF%E5%88%86) — zh.wikipedia.org
11. [Gaussian integral - Wikipedia](https://en.wikipedia.org/wiki/Gaussian_integral) — en.wikipedia.org
12. [Gaussian integrals are essential for calculating ...](https://www.facebook.com/100094746404967/posts/the-gaussian-integral-%EF%B8%8F%EF%B8%8Fthe-gaussian-integral-was-discovered-by-abraham-de-moivr/785389057962634) — facebook.com
13. [Gaussian Integral Derivation Explained - Normal Distribution](https://www.scribd.com/document/881290747/Gaussian-Integral-Differential-Equations) — scribd.com
14. [Jad Matta's Post](https://www.linkedin.com/posts/jadmatta_gaussian-integral-and-applications-the-activity-7485388096218390528-FPyi) — linkedin.com
