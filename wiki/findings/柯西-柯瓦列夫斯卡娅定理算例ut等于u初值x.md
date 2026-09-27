---
type: finding
title: "算例：u_t = u, u(x, 0) = x 的幂级数解 x + xt + …"
created: 2026-09-27
updated: 2026-09-27
tags: [柯西-柯瓦列夫斯卡娅定理, 幂级数, 比较系数, 算例]
related: [柯西-柯瓦列夫斯卡娅定理]
source: "[[10-数学指南实用数学手册--13-1135-一般的存在性结果--1siygdd]]"
confidence: high
replicated: null
sources: ["数学指南_实用数学手册/1.13.5 一般的存在性结果.md"]
---

# 算例：$u_t = u$，$u(x, 0) = x$ 的幂级数解

## 结果

源文档在陈述柯西-柯瓦列夫斯卡娅定理后给出（见 [[concepts/柯西-柯瓦列夫斯卡娅定理]]）

$$
u _ {t} = u, \quad u (x, 0) = x.
$$

取 $P := (0,0)$。由初始条件得 $u(P) = 0$，$u_x(P) = 1$，$u_{xx}(P) = 0$ 等；微分方程产生 $u_t(P) = u(P) = 0$，$u_{tt}(P) = u_t(P) = 0$，$u_{tx}(P) = u_x(P) = 1$。以这种方式在点 $P$ 的邻域中得到

$$
\begin{array}{c} u (\boldsymbol {x}, t) = u (\boldsymbol {P}) + u _ {x} (\boldsymbol {P}) x + u _ {t} (\boldsymbol {P}) t + \frac {1}{2} (u _ {x x} (\boldsymbol {P}) x ^ {2} + 2 u _ {t x} (\boldsymbol {P}) x t + u _ {t t} (\boldsymbol {P}) t ^ {2}) + \dots \\ = x + x t + \dots . \end{array}
$$

## 证据类型

这是源文档为演示「可以利用比较系数来求得解的幂级数展开」而给的**直接构造示例**，不是对定理的独立验证。它说明定理的构造性一侧：逐项求导比较系数即可逐阶确定幂级数系数。

## 相关页面

- [[concepts/柯西-柯瓦列夫斯卡娅定理]]
- [[sources/10-数学指南实用数学手册--13-1135-一般的存在性结果--1siygdd]]