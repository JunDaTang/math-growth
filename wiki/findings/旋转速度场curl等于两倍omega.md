---
type: finding
title: 旋转速度场满足 curl v = 2ω
source: "[[10-数学指南实用数学手册--20-198-环量闭积分曲线与斯托克斯积分定理--gv2pcd]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [向量分析, 旋转, 旋度, 角速度]
related: [旋转向量, 旋度, 闭积分曲线, 积分曲线]
sources: ["数学指南_实用数学手册/1.9.8 环量、闭积分曲线与斯托克斯积分定理.md"]
---

# 旋转速度场满足 curl v = 2ω

1.9.8 对旋转速度场 $\boldsymbol{v}(\boldsymbol{r}) := \boldsymbol{\omega} \times \boldsymbol{r}$ 给出的旋度结果（原文逐字引述）：

$$
\boxed {\operatorname{curl} v = 2 \omega .}
$$

> 这里, $\operatorname{curl} v$ 具有和旋转轴相同的方向, $\operatorname{curl} v$ 的长度等于粒子的角速度的两倍.

## 内容拆解

- **方向**：$\operatorname{curl} \boldsymbol{v}$ 与旋转轴 $\boldsymbol{\omega}$ 方向相同；
- **长度**：$|\operatorname{curl} \boldsymbol{v}| = 2|\boldsymbol{\omega}|$，即等于粒子角速度的两倍。

## 与 1.9.3 的呼应

1.9.3 的形变定理指出旋度描述旋转（[[findings/形变定理旋度描述旋转散度描述体积相对变化]]）。本式给出一个具体场上的精确对应：旋度向量就是角速度向量的两倍，方向沿转轴。

## 证据等级

教材陈述型结果，本节未给证明；未附文献编号。

## 相关页面

[[findings/旋转速度场v等于omega叉乘r]]、[[concepts/旋度]]、[[concepts/旋转向量]]。