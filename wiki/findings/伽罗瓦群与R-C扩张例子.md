---
type: finding
title: 伽罗瓦群定义与 R⊆C 扩张例子
created: 2026-09-27
updated: 2026-09-27
tags: [galois-theory, example]
related: [伽罗瓦群, 伽罗瓦扩张, 循环群, 复数域的哈密顿构造]
sources: ["数学指南_实用数学手册/2.6 伽罗瓦理论和代数方程.md"]
source: "[[10-数学指南实用数学手册--13-26-伽罗瓦理论和代数方程--1e86aig]]"
confidence: high
replicated: null
---

# 伽罗瓦群定义与 $\mathbb{R} \subseteq \mathbb{C}$ 扩张例子

## 定义

设 $K \subseteq E$ 是域扩张，其**伽罗瓦群** $G_K^E$（或 $\operatorname{Cal}(E|K)$，疑为 $\operatorname{Gal}(E|K)$ 的 OCR 讹误）定义为域 $E$ 的全部自同构的群，这些自同构平凡地作用于 $K$ 的所有元素。

有限域扩张 $K \subseteq E$ 称为**伽罗瓦扩张**，如果 $\mathrm{ord}\,G_K^E = [E:K]$。

## 例 3（$\mathbb{R} \subseteq \mathbb{C}$）

令 $\varphi: \mathbb{C} \to \mathbb{C}$ 保持所有实数不变。由 $\mathrm{i}^2=-1$ 得 $\varphi(\mathrm{i})^2=-1$，故 $\varphi(\mathrm{i})=\mathrm{i}$ 或 $-\mathrm{i}$，分别对应单位自同构与

$$
\varphi(a + b\mathrm{i}) := a - b\mathrm{i}
$$

（复共轭）。因此 $G_{\mathbb{R}}^{\mathbb{C}} = \{\mathrm{id}, \varphi\}$，$\varphi^2=\mathrm{id}$，且

$$
[\mathbb{C}:\mathbb{R}] = \mathrm{ord}\,G_{\mathbb{R}}^{\mathbb{C}} = 2.
$$

故 $\mathbb{C}|\mathbb{R}$ 是伽罗瓦扩张，伽罗瓦群是 **2 阶循环群**；由伽罗瓦群的单性可推出扩张的单性。由于 2 阶循环群没有任何子群，$\mathbb{R}$ 与 $\mathbb{C}$ 之间也不存在中间域扩张。

## 相关页面

[[伽罗瓦群]]、[[伽罗瓦扩张]]、[[域扩张]]、[[复数域的哈密顿构造]]
