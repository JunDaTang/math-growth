---
type: finding
title: 旋转速度场 v(r) = ω × r
source: "[[10-数学指南实用数学手册--20-198-环量闭积分曲线与斯托克斯积分定理--gv2pcd]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [向量分析, 旋转, 速度场, 向量积]
related: [旋转向量, 旋度, 闭积分曲线, 形变]
sources: ["数学指南_实用数学手册/1.9.8 环量、闭积分曲线与斯托克斯积分定理.md"]
---

# 旋转速度场 v(r) = ω × r

1.9.8 的例（原文逐字引述）：

> 例: 给定向量 $\omega$. 速度场
>
> $$
> \boxed {\boldsymbol {v} (\boldsymbol {r}) := \boldsymbol {\omega} \times \boldsymbol {r}}
> $$
>
> 对应于液体粒子沿轴 $\omega$ (正向) 旋转, 其角速度为 $|\omega|$.

## 内容要点

- 速度场由给定向量 $\boldsymbol{\omega}$ 与位置向量 $\boldsymbol{r}$ 的向量积给出：$\boldsymbol{v}(\boldsymbol{r}) := \boldsymbol{\omega} \times \boldsymbol{r}$；
- 物理解释：液体粒子绕轴 $\boldsymbol{\omega}$（正向）旋转；
- 角速度为 $|\boldsymbol{\omega}|$。

## 关联

本节例中的 $\boldsymbol{\omega}$ 与 1.9.3 讨论形变时的[[concepts/旋转向量]]同为旋转量记号，但两处语境不同：1.9.3 中 $\boldsymbol{\omega}$ 由位移场的旋度之半定义（[[findings/旋转向量定义为二分之一的旋度]]），本节则由外部给定并直接作为速度场参数。比较使用时须注意这一区别。

## 证据等级

教材陈述型例子，本节未给证明。

## 相关页面

[[findings/旋转速度场curl等于两倍omega]]、[[findings/旋转速度场积分曲线为绕轴同心圆]]、[[concepts/旋转向量]]。