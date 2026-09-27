---
type: query
title: "7.2.1 节置换矩阵恒等式 P·A = L·A 是否应为 P·A = L·R？"
tags: [线性方程组, 排版疑点, LR分解]
related: [高斯算法, LR分解, 线性方程组直接法]
created: 2026-09-28
updated: 2026-09-28
sources: ["数学指南_实用数学手册/7.2.1 线性方程组——直接法.md"]
---

# 7.2.1 节置换矩阵恒等式 P·A = L·A 是否应为 P·A = L·R？

## 疑点

7.2.1.1 节在定义 $R$、$L$ 与置换矩阵 $P$ 之后写道：

$$
\pmb{P} \cdot \pmb{A} = \pmb{L} \cdot \pmb{A} \quad (\mathrm{LR}\ \text{分解}).
$$

右端出现 $\pmb{L}\cdot\pmb{A}$，与名称「LR 分解」及上下文矛盾。

## 判断依据

- 同一节稍后给出的求解格式写作 $PA = LR$、$Lc - Pb = 0$、$Rx + c = 0$，并在推导中写 $P(Ax+b) = LRx + Pb$，均要求 $PA = LR$。
- 7.2.1.3 节用 $\det L = 1$、$\det R = \prod_k r_{kk}$、$\det P = (-1)^V$ 推出 $\det A$，也以 $PA = LR$ 为前提。
- 因此该式右端的 $A$ 极可能是 $R$ 的排印或 OCR 讹误。

## 待确认

该式右端是否确为 $R$；若确实如此，则需在源文档中订正为 $P \cdot A = L \cdot R$。

## Related
- [[queries/721节剩余r定义为x减xbar与扰动方程矛盾]]
