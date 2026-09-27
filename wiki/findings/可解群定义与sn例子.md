---
type: finding
title: 可解群定义与 S_n 例子
created: 2026-09-27
updated: 2026-09-27
tags: [群论, 伽罗瓦理论]
related: [concepts/可解群, concepts/交错群, concepts/伽罗瓦理论, entities/克莱因]
sources: ["数学指南_实用数学手册/2.5 代数结构.md"]
source: "10-数学指南实用数学手册--7-25-代数结构--necedq"
confidence: high
replicated: null
---

# 可解群定义与 S_n 例子

可解群：存在 $\{e\}=G_0\subseteq G_1\subseteq\dots\subseteq G_n=G$，使 $G_j\trianglelefteq G_{j+1}$ 且 $G_{j+1}/G_j$ 交换。

例 1：每个交换群可解。例 2：

- $\mathcal{S}_2$ 可解；
- $\mathcal{S}_3$ 可解，链 $\{e\}\subseteq\mathcal{A}_3\subseteq\mathcal{S}_3$；
- $\mathcal{S}_4$ 可解，链 $\{e\}\subseteq\mathcal{K}_4\subseteq\mathcal{A}_4\subseteq\mathcal{S}_4$，相关商群的阶 3、2、3 皆为素数，故对应商群是循环群从而是交换群；
- $n\ge5$ 时 $\mathcal{S}_n$ 不可解，因 $\mathcal{A}_5$ 是单群。

由伽罗瓦理论，这些结论是次数 $\ge5$ 的代数方程不可用根式解出的依据（见 2.6.5）。

> 直接引用。信心高。

## Related
- [[findings/sn与s4正规子群结构]]
