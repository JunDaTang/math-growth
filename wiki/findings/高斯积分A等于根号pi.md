---
type: finding
title: 高斯积分 A = √π
created: 2026-09-27
updated: 2026-09-27
tags: [高斯积分, 高斯分布, 极坐标, 累次积分, 经典结论]
related: [高斯积分在RN上等于根号pi的N次方, 极坐标下的二重积分, 乘积可分离函数的积分分解, 174节例2极坐标推导与重复行是否转写讹误]
source: "[[sources/10-数学指南实用数学手册--14-174-卡瓦列里原理累次积分--18vc3tg]]"
confidence: high
replicated: true
sources: ["数学指南_实用数学手册/1.7.4 卡瓦列里原理(累次积分).md"]
---

# 高斯积分 A = √π

## 结论（例 2，高斯分布）

```latex
A := \int_{-\infty}^{\infty} \mathrm{e}^{-x^{2}} \mathrm{d}x = \sqrt{\pi}.
```

## 源文给出的证明路径

源文称之为「一个优美、经典的技巧」：

1. 令

```latex
B := \int_{\mathbb{R}^{2}} \mathrm{e}^{-x^{2} - y^{2}} \mathrm{d}x \mathrm{d}y
```

由乘积分解（见 [[findings/乘积可分离函数的积分分解]]）得 $B = A \cdot A = A^2$。

2. 另一方面用极坐标（见 [[concepts/极坐标下的二重积分]]）计算 $B$：

```latex
B = \int_{r = 0}^{\infty} \left(\int_{0}^{2\pi} \mathrm{e}^{-r^{2}} r \mathrm{d}\varphi\right) \mathrm{d}r
= 2\pi \int_{0}^{\infty} \mathrm{e}^{-r^{2}} r \mathrm{d}r
= \lim_{R \to \infty} 2\pi \int_{0}^{R} \mathrm{e}^{-r^{2}} r \mathrm{d}r
```

```latex
= \lim_{R \to \infty} -\pi \mathrm{e}^{-r^{2}} |_{0}^{R}
= \lim_{R \to \infty} \pi (1 - \mathrm{e}^{-R^{2}}) = \pi .
```

3. 于是 $A^2 = \pi$，故 $A = \sqrt{\pi}$。

## 证据强度与说明

- 这是一个被完整证明的经典结论，属于直接证据。
- 证明的两个支柱是：乘积分解（把二维积分化为两个一维积分之积）与极坐标变换（利用旋转对称性）。
- 源文本处的记号存在若干转写／排版疑点（极限下标、$B$ 定义行重复、$r$ 与 $R$ 混用），见 [[queries/174节例2极坐标推导与重复行是否转写讹误]]；这些疑点不改变结论本身。

## 关联

- 本结果的一维因子推广到 $\mathbb{R}^N$ 即 $\int_{\mathbb{R}^{N}} \mathrm{e}^{-|x|^{2}} \mathrm{d}x = (\sqrt{\pi})^{N}$，见 [[findings/高斯积分在RN上等于根号pi的N次方]]（该页面此前引自 1.7.2 节，1.7.4 节是其原始出处）。