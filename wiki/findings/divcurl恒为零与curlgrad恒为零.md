---
type: finding
title: div curl 恒为零与 curl grad 恒为零
created: 2026-09-27
updated: 2026-09-27
tags: [外微分, 散度, 旋度, 梯度, 恒等式]
related: [庞加莱法则, 散度, 旋度, 梯度, 嘉当微分学, 向量分析的主要定理]
source: "[[10-数学指南实用数学手册--20-1911-经典向量分析与嘉当微分学的关系--1bdj8zw]]"
confidence: medium
replicated: null
sources: ["数学指南_实用数学手册/1.9.11 经典向量分析与嘉当微分学的关系.md"]
---

# div curl 恒为零与 curl grad 恒为零

《数学指南——实用数学手册》1.9.11 节指出，[[庞加莱法则]] (ii) 包括特例

$$
\operatorname{div}\operatorname{curl} H \equiv 0, \qquad \operatorname{curl}\operatorname{grad} V \equiv 0 .
$$

（原文写作 `divcurl H ≡ 0`，即 $\operatorname{div}(\operatorname{curl} H) \equiv 0$。）

## 主体归属澄清

- 这两条恒等式的**主体是庞加莱法则 $\mathrm{d}\mathrm{d}\omega = 0$**，它们是 $\mathrm{d}^2 = 0$ 在 $\mathbb{R}^3$ 向量分析语言下的翻译。
- 不要把它们归到 [[庞加莱引理]] 名下：引理处理的是"闭是否蕴含精确"的可解性问题，而这两条是算子复合的恒等消失。

## 物理与几何含义

- `div curl H ≡ 0`：旋度场是无源场（无散场）。这与 1.9.9 节 [[涡流的规定]] 的相容性条件一致。
- `curl grad V ≡ 0`：梯度场是无旋场（保守场）。这与 [[势与势函数]] 的可积性讨论一致。
- 从算子角度看，两条恒等式分别是 [[散度]]、[[旋度]]、[[梯度]] 的基本性质。

## 证据评估

- **类型**：标准恒等式的手册陈述，本节未给证明。
- **强度**：中（结论可靠，但本节未附推导与出处）。