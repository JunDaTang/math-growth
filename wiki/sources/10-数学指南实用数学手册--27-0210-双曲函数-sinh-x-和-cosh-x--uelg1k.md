---
type: source
title: Source: 数学指南_实用数学手册/0.2.10 双曲函数 $ sinh x$ 和 $ cosh x$.md
created: 2026-09-27
updated: 2026-09-27
tags: [数学指南, 双曲函数, 初等函数, 公式表, 0.2节]
related: [数学指南实用数学手册, 双曲正弦, 双曲余弦, 双曲函数与三角函数的关系, 双曲函数的幂级数, 双曲函数加法定理, 双曲函数倍角与半角公式, 双曲棣莫弗公式, 图0-34-双曲函数图像, 初等函数, 幂级数展开表, 一阶导数表, 等轴双曲线]
authors: []
year: 0
url: ""
venue: 《数学指南——实用数学手册》
sources: ["数学指南_实用数学手册/0.2.10 双曲函数 $ sinh x$ 和 $ cosh x$.md"]
---

# 《数学指南——实用数学手册》0.2.10 双曲函数 $\sinh x$ 和 $\cosh x$

本页是手册 0.2.10 节的入库摘要，主题为双曲正弦 $\sinh x$ 与双曲余弦 $\cosh x$ 的定义与全部初等恒等式。内容属公式清单型条目，全部公式对**复数** $x$（及 $y$）成立；个别公式（半角）限定于实变量。

## 定义与命名

对全体复数 $x$：

$$
\sinh x := \frac{\mathrm{e}^{x}-\mathrm{e}^{-x}}{2}, \qquad \cosh x := \frac{\mathrm{e}^{x}+\mathrm{e}^{-x}}{2}.
$$

正文注明读音：$\sinh$ 读作 “sinch”，$\cosh$ 读作 “cosh”。对实变量 $x$，其图像如图 0.34 所示。

「双曲函数」这一术语来自 $x = a\cosh t,\ y = b\sinh t,\ t \in \mathbb{R}$ 是双曲线的参数方程（源文档指向手册 0.1.7.4 节）。

## 与三角函数的关系

对所有复数 $x$：

$$
\sinh \mathrm{i} x = \mathrm{i} \sin x, \qquad \cosh \mathrm{i} x = \cos x.
$$

由此得到源文档中信息密度最高的方法论主张：关于双曲正弦和双曲余弦的**每个公式**都能由正弦和余弦函数得到。所给示例为：由对任意复数 $x$ 有 $\cos^2 \mathrm{i}x + \sin^2 \mathrm{i}x = 1$，可得到

$$
\cosh^{2} x - \sinh^{2} x = 1.
$$

细节与证据强度评估见 [[双曲函数与三角函数的关系]]。

## 恒等式清单（原文逐字保留）

偶性与奇性：

$$
\sinh(-x) = -\sinh x, \qquad \cosh(-x) = \cosh x.
$$

复数域中的周期性：

$$
\sinh(x + 2\pi \mathrm{i}) = \sinh x, \qquad \cosh(x + 2\pi \mathrm{i}) = \cosh x.
$$

幂级数：

$$
\sinh x = x + \frac{x^{3}}{3!} + \frac{x^{5}}{5!} + \frac{x^{7}}{7!} + \dots,
\qquad
\cosh x = 1 + \frac{x^{2}}{2!} + \frac{x^{4}}{4!} + \frac{x^{6}}{6!} + \dots .
$$

导数：

$$
\frac{\mathrm{d}\sinh x}{\mathrm{d}x} = \cosh x, \qquad \frac{\mathrm{d}\cosh x}{\mathrm{d}x} = \sinh x.
$$

加法定理：

$$
\begin{array}{l}
\sinh(x \pm y) = \sinh x \cosh y \pm \cosh x \sinh y, \\
\cosh(x \pm y) = \cosh x \cosh y \pm \sinh x \sinh y.
\end{array}
$$

倍角公式：

$$
\sinh 2x = 2 \sinh x \cosh x, \qquad \cosh 2x = \sinh^{2} x + \cosh^{2} x.
$$

半角公式：

$$
\sinh \frac{x}{2} =
\begin{cases}
\sqrt{\frac{1}{2}(\cosh x - 1)}, & x \geqslant 0, \\
-\sqrt{\frac{1}{2}(\cosh x - 1)}, & x < 0,
\end{cases}
$$

$$
\cosh \frac{x}{2} = \sqrt{\frac{1}{2}(\cosh x + 1)}, \qquad x \in \mathbb{R}.
$$

棣莫弗公式：

$$
(\cosh x \pm \sinh x)^{n} = \cosh n x \pm \sinh n x, \qquad n = 1, 2, \dots .
$$

和差化积：

$$
\sinh x \pm \sinh y = 2 \sinh \frac{1}{2}(x \pm y) \cosh \frac{1}{2}(x \mp y),
$$

$$
\cosh x + \cosh y = 2 \cosh \frac{1}{2}(x + y) \cosh \frac{1}{2}(x - y),
$$

$$
\cosh x - \cosh y = 2 \sinh \frac{1}{2}(x + y) \sinh \frac{1}{2}(x - y).
$$

## 图 0.34

图 0.34 由两幅子图组成：(a) $y = \sinh x$、(b) $y = \cosh x$。**本 wiki 中两张图片均未能加载**，视觉细节缺失；正文亦未以文字复述曲线特征（如 $\cosh$ 在 $x = 0$ 处取极小值 1、$\sinh$ 过原点且关于原点对称）。因此「对实变量 $x$，其图像如图 0.34 所示」这一指向在库内证据断裂。

- 子图 (a)：`media/10-数学指南实用数学手册--27-0210-双曲函数-sinh-x-和-cosh-x--uelg1k/001-32158e7b953453bb7c848ee4addc01790c5f566b404e717401646d346ad6928d.jpg`
- 子图 (b)：`media/10-数学指南实用数学手册--27-0210-双曲函数-sinh-x-和-cosh-x--uelg1k/002-9a87ae32863303d51383553dd9ff51646f86eb17f126c8bdf1846db3f4d5f149.jpg`

## 排版疑点

源文档在「半角」与「棣莫弗公式」两处的小标题与公式归属发生错位：$\cosh \frac{x}{2} = \sqrt{\frac{1}{2}(\cosh x + 1)}$ 一行被置于「棣莫弗公式」小标题之后，而棣莫弗公式本身紧接其后。按内容归属，$\cosh \frac{x}{2}$ 应属「半角」条目。详见 [[0210节半角与棣莫弗公式小标题错位]]。

## 关联

- 手册主条目：[[数学指南实用数学手册]]
- 与 0.8 节微分表对照：[[一阶导数表]]、[[初等函数]]
- 与 0.7.2 幂级数展开表对照：[[幂级数展开表]]、[[幂级数]]
- 同属 0.2 节但对象不同：[[等轴双曲线]]（$y = b/x$ 型，与 $x = a\cosh t,\ y = b\sinh t$ 参数化的双曲线**不是同一对象**）

<!-- llm-wiki:embedded-images -->
## Embedded Images

### Document

![图片内容未能加载（显示为不支持的内容类型），无法直接观察其视觉细节。根据上下文，该图片位于双曲函数恒等式推导之后，紧邻的公式为 cosh x − cosh y = 2 sinh ½(x + y) sinh ½(x − y)，其后引用的文件名表明图片出自《数学指南：实用数学手册》第27页关于双曲函数 sinh x 和 cosh x 的部分。因此该图很可能与双曲函数 sinh x 和 cosh x 的定义、图像或相关公式有关，但具体内容无法确认。](../media/10-数学指南实用数学手册--27-0210-双曲函数-sinh-x-和-cosh-x--uelg1k/001-32158e7b953453bb7c848ee4addc01790c5f566b404e717401646d346ad6928d.jpg)
![图片内容未能成功加载，无法直接查看其具体视觉细节。根据文件名信息，该图出自《数学指南：实用数学手册》第27-0210部分，主题为双曲函数 sinh x 和 cosh x。推测图中可能包含这两个双曲函数的定义、公式或函数曲线，但具体内容（如坐标轴、数值、标注文字等）无法确认。](../media/10-数学指南实用数学手册--27-0210-双曲函数-sinh-x-和-cosh-x--uelg1k/002-9a87ae32863303d51383553dd9ff51646f86eb17f126c8bdf1846db3f4d5f149.jpg)
<!-- llm-wiki:embedded-images -->
