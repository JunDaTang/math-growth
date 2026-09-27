---
type: finding
title: 分式函数 y = b/x 的图像是以两坐标轴为渐近线的等轴双曲线
source: "[[10-数学指南实用数学手册--9-0215-有理函数--111cnov]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 有理函数, 双曲线, 渐近线]
related: [等轴双曲线, 有理函数, 有理函数的极点, 双曲线的标准方程与渐近线]
sources: ["数学指南_实用数学手册/0.2.15 有理函数.md"]
---

# 分式函数 $y = b/x$ 的图像是以两坐标轴为渐近线的等轴双曲线

## 陈述

对固定实数 $b>0$，函数

```latex
y = \frac{b}{x}, \quad x \in \mathbb{R},\ x \neq 0
```

的图像是以 $x$ 轴和 $y$ 轴为渐近线的等轴双曲线，其顶点为 $S_{\pm} = (\pm\sqrt{b}, \pm\sqrt{b})$。

## 支持证据

极限计算直接给出渐近线：

```latex
\lim_{x \to \pm\infty} \frac{b}{x} = 0, \qquad \lim_{x \to \pm 0} \frac{b}{x} = \pm\infty .
```

前式对应水平渐近线 $y=0$，后式表明 $x=0$ 是极点并对应竖直渐近线 $x=0$。

## 来源与强度

来源：《数学指南——实用数学手册》0.2.15.1（图 0.37）。属教科书定义性陈述，结论充分建立。此处为直接证据，非推断。

## 相关

- [[concepts/等轴双曲线]]
- [[concepts/有理函数的极点]]

## Related
- [[findings/线性分式函数可经坐标平移化为标准形]]
