---
type: query
title: 7.2.3.2 节 A'' = A'U 元素公式中 a''_iq 右端首项是否应为 a'_ip？
created: 2026-09-28
updated: 2026-09-28
tags: [勘误, 数值线性代数, 雅可比方法]
related: [雅可比旋转矩阵, 雅可比方法求矩阵特征值]
sources: ["数学指南_实用数学手册/7.2.3 特征值问题.md"]
---

# 7.2.3.2 节 $A'' = A'U$ 元素公式中 $a''_{iq}$ 右端首项是否应为 $a'_{ip}$？

## 问题

源文在给出 $A'' = A'U$ 的元素时写作

$$
\left\{
\begin{array}{l}
a''_{ip} = a'_{ip}\cos\varphi - a'_{iq}\sin\varphi,\\
a''_{iq} = a''_{ip}\sin\varphi + a'_{iq}\cos\varphi, \qquad i = 1,2,\dots,n,\\
a''_{ij} = a'_{ij}, \quad j \neq p,q,
\end{array}
\right.
$$

第二式右端首项使用了**双撇**记号 $a''_{ip}$。

## 疑点分析

- 同一组公式中的第一式为 $a''_{ip} = a'_{ip}\cos\varphi - a'_{iq}\sin\varphi$，即 $a''_{ip}$ 是**待求量**；若第二式的首项确为 $a''_{ip}$，则该式成为同一 $i$ 上两个待求量的联立关系，需要对每个 $i$ 解一次二元方程组才可用，与紧随其后的 $a''_{pq}$、$a''_{pp}$、$a''_{qq}$ 表达式所体现的「直接由 $a'$（或 $a$）显式给出 $a''$」的写法不一致。
- 若按右乘 $A'' = A'U$ 的直接计算：$a''_{iq} = a'_{ip}u_{pq} + a'_{iq}u_{qq} = a'_{ip}\sin\varphi + a'_{iq}\cos\varphi$，即第二式首项应为**单撇**的 $a'_{ip}$。
- 这与第一式 $a''_{ip} = a'_{ip}\cos\varphi - a'_{iq}\sin\varphi$（对应 $u_{pp}=\cos\varphi$、$u_{qp}=-\sin\varphi$）形式对称，符合 $U(p,q,\varphi)$ 的旋转结构。

## 待确认

源文此处是否属于排版/转写笔误，即将 $a'_{ip}$ 误排为 $a''_{ip}$？需要与《数学指南——实用数学手册》原书或德文底本核对。

## 相关页面

[[雅可比旋转矩阵]]、[[雅可比方法求矩阵特征值]]、[[10-数学指南实用数学手册--9-723-特征值问题--1u0tufj]]。
