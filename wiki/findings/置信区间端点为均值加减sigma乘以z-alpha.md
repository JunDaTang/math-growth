---
type: finding
title: 置信区间端点为均值加减 sigma 乘以 z-alpha
created: 2026-09-27
updated: 2026-09-27
tags: [数理统计, 置信区间, 正态分布]
related: [置信区间, z-alpha分位数, 正态分布]
sources: ["数学指南_实用数学手册/0.4.2 理论分布函数.md"]
source: "[[10-数学指南实用数学手册--10-042-理论分布函数--118ygtx]]"
confidence: high
replicated: null
---

# 置信区间端点为均值加减 sigma 乘以 z-alpha

源给出正态分布下 $\alpha$ 置信区间的对称端点公式：

$$
x_\alpha^+ = \mu + \sigma z_\alpha,\qquad x_\alpha^- = \mu - \sigma z_\alpha.
$$

并以 $\mu = 10$、$\sigma = 2$、$\alpha = 0.01$（$z_\alpha = 2.6$）验证：

$$
x_\alpha^+ = 15.2,\qquad x_\alpha^- = 4.8,
$$

对应概率 $1 - \alpha = 0.99$。

## 证据类型

公式为源中直接陈述；数值示例为源中直接给出的算例。两段皆为理论性内容，`replicated` 记为 null。$z_\alpha$ 仅由 [[z-alpha分位数]] 表给出，源未给出其形式化定义。

## Related
- [[findings/正态密度在均值处取极大值且sigma越小越集中]]
