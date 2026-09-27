---
type: finding
title: 重力场势能等于 mgz
created: 2026-09-27
updated: 2026-09-27
tags: [physics, gravity, potential-energy, example]
related: [shi-neng, li-chang, di-ka-er-zuo-biao-xi, zhong-li-chang-de-gong-yu-shi-neng, shi-yu-shi-han-shu]
sources: ["数学指南_实用数学手册/1.9.5 功、势能和积分曲线.md"]
source: "[[10-数学指南实用数学手册--12-195-功势能和积分曲线--1a5dngy]]"
confidence: high
replicated: false
---

# 重力场势能等于 mgz

## 结论

源文 1.9.5 节的例子：令 $\boldsymbol{F} = -mg\boldsymbol{k}$ 为笛卡儿坐标系下作用在质量为 $m$ 的石块上的重力（$g$ 是重力加速度），则势能为

$$
U = mgz .
$$

验证：$\operatorname{grad} U = U_z \boldsymbol{k} = -\boldsymbol{F}$。

## 物理解释

若石块从高为 $z > 0$ 处落到 $z = 0$ 处，则 $W = U = mgz$ 是地球引力场所做的功；在落地时它转换成了热能（源文括注：「和动能 —— 校者」）。

## 适用对象边界

本结论针对**均匀（常数）重力场** $\boldsymbol{F} = -mg\boldsymbol{k}$。它不应与 [[concepts/太阳引力公式]] 所描述的平方反比中心力场混同——后者对应的势是不同的函数形式（例如 $U \propto -1/r$），源文并未在本节讨论。

## 证据类型

源文正文算例，附以梯度验证，属直接证据。

## Related
- [[findings/重力场势能与中心力场势函数不可混用]]
