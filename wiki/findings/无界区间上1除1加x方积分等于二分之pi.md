---
type: finding
title: ∫₀^∞ dx/(1+x²) = π/2 及全直线上的积分 = π
source: "[[10-数学指南实用数学手册--11-16-单实变函数的积分--1exp43p]]"
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 微积分, 积分, 广义积分]
related: [无界区间上的积分, 微积分基本定理, 10-数学指南实用数学手册--11-16-单实变函数的积分--1exp43p]
confidence: high
replicated: null
sources: ["数学指南_实用数学手册/1.6 单实变函数的积分.md"]
---

# ∫₀^∞ dx/(1+x²) = π/2 及全直线上的积分 = π

## 内容

1.6.1 节（直观引入）与 1.6.6 节（正式定义与例）均给出：

$$
\int_{0}^{\infty} \frac{\mathrm{d}x}{1+x^{2}} = \lim_{b \to +\infty} \int_{0}^{b} \frac{\mathrm{d}x}{1+x^{2}} = \frac{\pi}{2}.
$$

1.6.6 节进一步给出

$$
\int_{-\infty}^{0} \frac{\mathrm{d}x}{1+x^{2}} = \lim_{b \to -\infty}(-\arctan b) = \frac{\pi}{2},
\qquad
\int_{-\infty}^{+\infty} \frac{\mathrm{d}x}{1+x^{2}} = \frac{\pi}{2} + \frac{\pi}{2} = \pi.
$$

## 推导依据

$$
\int_{0}^{b}\frac{\mathrm{d}x}{1+x^{2}} = \arctan x\Big|_{0}^{b} = \arctan b - \arctan 0 = \arctan b,
$$

即由[[微积分基本定理]]得到原函数 $\arctan x$ 后取极限。该例同时满足[[无界区间上的积分]]的存在性判别准则（$|f(x)| \leqslant 1/(1+|x|)^2$，$\alpha = 2 > 1$）。

## Related
- [[findings/无界函数1除根号x在0到1上积分为2]]
