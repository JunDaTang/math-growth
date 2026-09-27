---
type: finding
title: N 体牛顿定律公式 (1.163) 与初始条件 (1.164)
source: "[[10-数学指南实用数学手册--14-196-对力学的守恒律的应用--191o34i]]"
confidence: high
replicated: false
created: 2026-09-27
updated: 2026-09-27
tags: [经典力学, 牛顿定律, 运动方程, 初始条件]
related: [N体问题, 牛顿基本运动定律, 轨道]
sources: ["数学指南_实用数学手册/1.9.6 对力学的守恒律的应用.md"]
---

# N 体牛顿定律公式 (1.163) 与初始条件 (1.164)

**来源**：《数学指南——实用数学手册》1.9.6 节。

**直接证据（原文）**：经典力学中 $N$ 体（质点）运动的牛顿定律为

$$
\boxed{m_{j} \boldsymbol{r}_{j}^{\prime \prime}(t) = \boldsymbol{F}_{j}(\boldsymbol{r}_{1}, \dots, \boldsymbol{r}_{N}, \boldsymbol{r}_{1}^{\prime}, \dots, \boldsymbol{r}_{N}^{\prime}, t), \quad j = 1, \dots, N,}\tag{1.163}
$$

其中 $m_j$ 是第 $j$ 个质点的质量，$F_j$ 表示作用在第 $j$ 个质点上的力；方程的解是轨道 $r_j = r_j(t)$，$j = 1, \cdots, N$。初始时刻 $t = 0$ 的初始位置和速度为

$$
\boldsymbol{r}_{j}(0) = \boldsymbol{r}_{j 0}, \quad \boldsymbol{r}_{j}^{\prime}(0) = \boldsymbol{r}_{j 1}, \quad j = 1, \dots, N.\tag{1.164}
$$

原文令 $r := (r_1, \cdots, r_N)$ 以简化记号。

**推断（非原文直接陈述）**：该方程是 1.9.1 节单体形式 $F = ma$ 的多体并列形式，耦合来自每个 $F_j$ 依赖于全部位置与速度。

**备注**：这是本节的起始陈述，属于后续所有推导的定义性基础，证据强度为陈述性。