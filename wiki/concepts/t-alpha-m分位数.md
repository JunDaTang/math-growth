---
type: concept
title: t-alpha-m分位数（$t_{\alpha,m}$）
created: 2026-09-27
updated: 2026-09-27
tags: [数理统计, t分布, 分位数, 置信限]
related: [均值的置信限, 自由度, 误差概率, 测量序列, t-alpha-m分位数的单双侧约定]
sources: ["数学指南_实用数学手册/0.4.4 测量序列的统计计算.md"]
---

# t-alpha-m分位数（$t_{\alpha,m}$）

## 定义与作用

$t_{\alpha,m}$ 是由误差概率 $\alpha$ 与自由度 $m$ 确定的 $t$ 分布分位数。在 0.4.4 节中，它作为 [[均值的置信限]] 的乘子出现：

$$
\bar{x} - t_{\alpha,m} \frac{\Delta x}{\sqrt{n}} \leqslant \mu \leqslant \bar{x} + t_{\alpha,m} \frac{\Delta x}{\sqrt{n}}.
$$

其中 $m = n - 1$（见 [[自由度]]），$\alpha$ 为 [[误差概率]]。

## 查表方式

$t_{\alpha,m}$ 的数值由 0.4.6.3 的表给出。手册中给出的例证为：$\alpha = 0.01$、$m = 7$ 时 $t_{\alpha,m} = 3.5$。

## 与置信水平的关系

若命题的误差概率为 $\alpha$，则区间以概率 $1 - \alpha$ 覆盖真值 $\mu$；因此 $\alpha$ 越小，$t_{\alpha,m}$ 越大，区间越宽。这与 [[置信区间]] 的一般语义一致，但与 [[z-alpha分位数]] 不同：后者适用于已知 $\sigma$ 或大样本的场合，而 $t_{\alpha,m}$ 用于样本量小、以经验标准差 $\Delta x$ 代替 $\sigma$ 的场合。

## 待澄清问题

$t_{\alpha,m}$ 是单侧还是双侧分位数尚无明文说明。例证 $\alpha = 0.01, m = 7 \Rightarrow 3.5$ 更符合双侧约定，详见 [[t-alpha-m分位数的单双侧约定]]。
