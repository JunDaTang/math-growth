---
type: concept
title: 微分算子 d
created: 2026-09-27
updated: 2026-09-27
tags: [数学分析, 微分算子, 莱布尼茨, 形式微分]
related: [莱布尼茨微分学, 全微分, 张量积, 嘉当微分学, 微分算子, 弗雷歇微分]
sources: ["数学指南_实用数学手册/1.5.10 弗雷歇微分.md"]
---

# 微分算子 d

在 1.5.10.3 节中，**微分算子 $\mathrm{d}$** 被定义为把偏导算子与微分 $\mathrm{d}x_j$ 组合起来的形式算子：

$$
\mathrm{d}:=\sum_{j=1}^{N}\mathrm{d}x_j\partial_j .
$$

若约定 $\partial_j\otimes f(x):=\partial_jf(x)$，则全微分公式 (1.87) 可写成

$$
\mathrm{d}f(x)=\mathrm{d}\otimes f(x).
$$

同理，二阶微分写作

$$
\mathrm{d}^{2}f(x)=\mathrm{d}\otimes\mathrm{d}f(x), \tag{1.90}
$$

即莱布尼茨微分学的二阶算子是 $\mathrm{d}^{2}=\mathrm{d}\otimes\mathrm{d}$。

## 与嘉当体系中 d 的关系

嘉当微分学使用同一个符号 $\mathrm{d}$，但由 $\mathrm{d}^{2}=\mathrm{d}\wedge\mathrm{d}$ 给出，并因 $\wedge$ 反交换而有 $\mathrm{d}^2=0$（记忆式：$\mathrm{d}\wedge(\mathrm{d}\wedge\omega)=(\mathrm{d}\wedge\mathrm{d})\wedge\omega=0$）。因此同一个 $\mathrm{d}$ 在两大体系中的二阶行为由所配的积（$\otimes$ 或 $\wedge$）决定。

## 注意区分

本页的 $\mathrm{d}$ 与 1.5.4 节中记为 [[微分算子]] 的概念**含义不同**：后者属于对微分算子的变换（如拉普拉斯算子的极坐标表示），并非这里由 $\mathrm{d}x_j\partial_j$ 定义的形式微分算子。二者仅在「算子作用于函数」这一表层相似。

## 相关

- [[莱布尼茨微分学]]
- [[嘉当微分学]]
- [[全微分]]
- [[张量积]]