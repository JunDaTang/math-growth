---
type: query
title: 1.13.4.1 节能量导数推导中的第二项 $u_x u_{xx}$ 是否应为 $u_x u_{xt}$？
created: 2026-09-27
updated: 2026-09-27
tags: [偏微分方程, 能量方法, 文本疑义]
related: [能量方法, 问题1425弦振动至多一个光滑解]
sources: ["数学指南_实用数学手册/1.13.4 关于唯一性的一般原理.md"]
---

# 1.13.4.1 节能量导数推导中的第二项 $u_x u_{xx}$ 是否应为 $u_x u_{xt}$？

## 疑点

源文献在证明 $E'(t) = 0$ 时写出

$$
E ^ {\prime} (t) = \int_ {0} ^ {L} (u _ {t} u _ {t t} + u _ {x} u _ {x x}) \mathrm{d} x = \int_ {0} ^ {L} u _ {t} (u _ {t t} - u _ {x x}) \mathrm{d} x + u _ {x} (x, t) u _ {t} (x, t) \bigg | _ {0} ^ {L} = 0 .
$$

但按能量泛函 $E = \int_0^L \frac{1}{2}(u_t^2 + u_x^2)\,\mathrm{d}x$ 求导，被积函数中的第二项应为 $u_x u_{xt}$，即

$$E'(t) = \int_0^L (u_t u_{tt} + u_x u_{xt})\,\mathrm{d}x .$$

只有当第二项为 $u_x u_{xt}$ 时，分部积分

$$\int_0^L u_x u_{xt}\,\mathrm{d}x = u_x u_t\big|_0^L - \int_0^L u_{xx} u_t\,\mathrm{d}x$$

才会得到文献右端所示的体积分 $\int_0^L u_t(u_{tt} - u_{xx})\,\mathrm{d}x$ 与边界项 $u_x u_t\big|_0^L$。

## 待核实

- 出版文本是否确有 $u_x u_{xx}$ 这一处笔误，或原文另有约定（例如把 $u_{xx}$ 用作 $u_{xt}$ 的排印？）。
- 若为笔误，后续版本是否已更正。

## 影响

不影响结论（$E'(t) = 0$ 与唯一性结果均成立），但影响该推导的可复算性与教学中引用时的忠实度。

## 相关

[[findings/问题1425弦振动至多一个光滑解]]、[[concepts/能量方法]]、[[sources/10-数学指南实用数学手册--15-1134-关于唯一性的一般原理--z2slyw]]。