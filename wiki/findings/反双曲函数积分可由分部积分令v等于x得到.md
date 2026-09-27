---
type: finding
title: 反双曲函数积分可由分部积分令 v = x 得到
source: "[[10-数学指南实用数学手册--11-095-不定积分表-4--1xsa9lg]]"
confidence: high
replicated: true
created: 2026-09-27
updated: 2026-09-27
tags: [分部积分, 反双曲函数, 不定积分, 公式推导]
related: [含反双曲函数的积分, 反双曲函数的导数, 分部积分公式, 表095不定积分表-4]
sources: ["数学指南_实用数学手册/0.9.5 不定积分表-4.md"]
---

# 反双曲函数积分可由分部积分令 v = x 得到

## 观察

《数学指南——实用数学手册》0.9.5.5 节的四条公式（502–505，见 [[entities/表095不定积分表-4]]）具有完全相同的结构：

```latex
\int u(x)\,\mathrm{d}x = x\,u(x) - \int x\,u'(x)\,\mathrm{d}x
```

其中 $u(x)$ 依次取 $\operatorname{arsinh}(x/\alpha)$、$\operatorname{arcosh}(x/\alpha)$、$\operatorname{artanh}(x/\alpha)$、$\operatorname{arcoth}(x/\alpha)$。这正是 [[concepts/分部积分公式]] 中令 $v = x$ 的特例（等价于令 $\mathrm{d}v = \mathrm{d}x$ 并取 $v = x$）。

## 证据

对四条的余项积分 $\int x\,u'(x)\,\mathrm{d}x$ 逐一计算（使用 [[concepts/反双曲函数的导数]]）：

| 条目 | $u(x)$ | $x\,u'(x)$ | 余项积分 |
|------|--------|------------|----------|
| 502 | $\operatorname{arsinh}(x/\alpha)$ | $x/\sqrt{x^{2}+\alpha^{2}}$ | $\sqrt{x^{2}+\alpha^{2}}$ |
| 503 | $\operatorname{arcosh}(x/\alpha)$ | $x/\sqrt{x^{2}-\alpha^{2}}$ | $\sqrt{x^{2}-\alpha^{2}}$ |
| 504 | $\operatorname{artanh}(x/\alpha)$ | $\alpha x/(\alpha^{2}-x^{2})$ | $-\frac{\alpha}{2}\ln(\alpha^{2}-x^{2})$ |
| 505 | $\operatorname{arcoth}(x/\alpha)$ | $\alpha x/(\alpha^{2}-x^{2})$ | $-\frac{\alpha}{2}\ln(x^{2}-\alpha^{2})$ |

将余项取负后加回 $x\,u(x)$，即得手册给出的四条结果，符号与系数完全一致。

## 意义

此发现说明 0.9.5.5 子节无需任何专门技巧：整个族都是「被积函数含反函数」这一常见情形下 $v = x$ 分部积分的机械产物，与 [[findings/积分基本定理由分部积分令v等于1得到]] 记录的技巧同源。它与 501（`arccot` 的降幂递推，见 [[concepts/积分递推公式]]）形成对照：后者是递归型条目，前者是闭式条目。

## 置信度与重复性

- 置信度：高。四条的推导均逐项闭合，无自由参数需估计。
- 重复性：公式本身在手册内一次性给出，本页结论由独立求导验算复现（见 [[findings/095节501至505条目逐条求导验算正确]]）。
