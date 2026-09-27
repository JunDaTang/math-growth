---
type: finding
title: 例 3 的代换等价于 t = sinh x
source: "[[10-数学指南实用数学手册--8-094-重要代换--12ghtkn]]"
confidence: high
replicated: false
tags: [example, hyperbolic, substitution]
related: [第一类积分的指数代换, 代换公式的记忆形式, 双曲正弦]
created: 2026-09-27
updated: 2026-09-27
sources: ["数学指南_实用数学手册/0.9.4 重要代换.md"]
---

# 例 3 的代换等价于 t = sinh x

## 观察

源文件例 3 说明式 (0.56) 对计算 $J:=\int \sinh^{n}x\cosh x\,\mathrm{d}x$ 很有帮助：

$$
J:=\int \sinh^{n}x\,\mathrm{d}\sinh x=\frac{\sinh^{n+1}x}{n+1},\quad n=1,2,\dots
$$

并明确指出：**这种方法相当于作了代换 $t=\sinh x$**。

## 证据类型

源文件直接给出的等价性陈述。式 (0.56) 即 [[代换公式的记忆形式]]（0.9.2 节），其形式把「凑微分」包装为 $\int f\,\mathrm{d}g=\int f g'\,\mathrm{d}x$ 式的记忆规则。

## 说明

- 该例说明第一类积分并不必然经由 $t=\mathrm{e}^{x}$：当被积函数恰好构造成 $\sinh^{n}x\,\mathrm{d}(\sinh x)$ 时，$t=\sinh x$ 是更直接的代换。
- 与 [[例2指出双曲平方积分无需指数代换]] 属同一组「代换非必要」的示例。
- 复制状态未知。
