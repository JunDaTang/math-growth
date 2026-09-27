---
type: query
title: 1.12.1.3 重标度推导中记号 N 与 𝓝 混用
created: 2026-09-27
updated: 2026-09-27
tags: [疑点, 记号, 转录]
related: [重标度, 逻辑斯谛方程, 10-数学指南实用数学手册--11-1121-引导性的例子--2uo3hb]
sources: ["数学指南_实用数学手册/1.12.1 引导性的例子.md"]
---

# 1.12.1.3 重标度推导中记号 N 与 𝓝 混用

源文 1.12.1.3 重标度处引进新变量写作

```latex
N(t) = \gamma \mathcal N, \quad t = \delta\tau,
```

但紧接着的推导却写作

```latex
\frac{\mathrm{d}N}{\mathrm{d}t} = \frac{\mathrm{d}(\gamma\mathcal N)}{\mathrm{d}\tau}\frac{\mathrm{d}\tau}{\mathrm{d}t}
= \gamma\mathcal N'(\tau)\frac{1}{\delta}
= \alpha\gamma\mathcal N(\tau) - \beta\gamma^2\mathcal N(\tau)^2 .
```

左端 $\mathrm dN/\mathrm dt$ 使用旧记号 $N$，右端使用新记号 $\gamma\mathcal N$，属于同一行内符号混用。此外，归一化后方程 (1.209) 以 $\mathcal N$ 为未知函数，而 1.12.1.3 稳定性段落又出现「该系统发展为平衡态 $N\equiv 1$」，与 $\mathcal N\equiv 1$ 混用。

**待办**：核对原书排版，确认 $N$ 与 $\mathcal N$ 是否确为不同符号，还是转录过程中 $\mathcal N$ 被误写为 $N$。

## 相关页面

[[重标度]]、[[逻辑斯谛方程]]、[[10-数学指南实用数学手册--11-1121-引导性的例子--2uo3hb]]。