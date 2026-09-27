---
type: finding
title: 局部微分同胚定理要求 det f′(p) ≠ 0
created: 2026-09-27
updated: 2026-09-27
tags: [逆映射定理, 雅可比行列式, 局部可逆性]
related: [局部微分同胚定理, 微分同胚, 雅可比行列式, 局部Ck类]
sources: ["数学指南_实用数学手册/1.5.7 逆映射.md"]
source: "[[10-数学指南实用数学手册--7-157-逆映射--3o8794]]"
confidence: high
replicated: null
---

# 局部微分同胚定理要求 det f′(p) ≠ 0

**结论（直接来自源文档）：** 令 $1 \leqslant k \leqslant \infty$。若 $f: M \subseteq \mathbb{R}^N \to \mathbb{R}^N$ 在 $p$ 的一个开邻域 $V(p)$ 内是 $C^k$ 类的，且 $\det f'(p) \neq 0$，则 $f$ 在 $p$ 处是局部 $C^k$ 类[[微分同胚]]。

**条件的局部性：** 两个前提都只在 $p$ 附近提出——$C^k$ 类要求在开邻域 $V(p)$ 内成立（[[局部Ck类]]），非退化条件只在该单点 $p$ 处成立（[[雅可比行列式]]）。

**结论的局部性：** 原书脚注明确指出，结论指 $f$ 是从某一恰当选取的开邻域 $U(p)$ 到开邻域 $U(f(p))$ 的 $C^k$ 类微分同胚，而非在整个定义域上可逆。

**证据类型：** 原书定理陈述，标准结果，confidence 高。

## Related
- [[findings/紧集上的连续双射必为同胚]]
- [[findings/例二元映射在雅可比非零处局部微分同胚]]
