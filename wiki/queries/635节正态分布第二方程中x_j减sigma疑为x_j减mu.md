---
type: query
title: 6.3.5 节正态分布特例第二方程中 (x_j − σ)² 是否为 (x_j − μ)² 之误？
created: 2026-09-27
updated: 2026-09-27
tags: [数理统计, 最大似然法, 正态分布, 印刷疑点]
related: [最大似然方程组, 高斯正态分布, 最大似然法]
sources: ["数学指南_实用数学手册/6.3.5 参数估计的最大似然方法.md"]
---

# 6.3.5 节正态分布特例第二方程中 (x_j − σ)² 是否为 (x_j − μ)² 之误？

## 问题

将正态分布密度代入 (6.37) 后，原书给出的方程组为：

```latex
\sum_{j=1}^{n} \left(\mu - x_j\right) = 0,
\qquad
-\frac{n}{\sigma} + \sum_{j=1}^{n} \frac{\left(x_j - \sigma\right)^2}{\sigma^3} = 0.
```

第二式的分子写作 $(x_j - \sigma)^2$，即以**标准差 $\sigma$** 与观测值相减。

## 证据

同页给出的偏导公式为

```latex
\frac{\partial \varphi}{\partial \sigma}
  = \left(-\frac{1}{\sigma} + \frac{(\mu - x)^2}{\sigma^3}\right)\varphi,
```

分子应为 $(\mu - x)^2$（等价于 $(x_j - \mu)^2$），而非 $(x_j - \sigma)^2$。此外，紧随其后的结果式使用了 $\sigma^2 = \frac{1}{n}\sum (x_j - \mu)^2$，也可反证中间一步是笔误。

## 建议处理

按分子为 $(x_j - \mu)^2$ 理解该方程；建议在勘误中记录。

## 相关页面

- [[最大似然方程组]]、[[高斯正态分布]]、[[最大似然法]]