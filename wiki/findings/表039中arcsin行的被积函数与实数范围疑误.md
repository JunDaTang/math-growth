---
type: finding
title: 表 0.39 中 arcsin 行的被积函数与实数范围疑误
source: "[[10-数学指南实用数学手册--11-091-初等函数的积分--1xupt5l]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [积分表, 转写疑误, arcsin, 定义域]
related: [表039基本积分, 原函数, 初等函数的积分]
sources: ["数学指南_实用数学手册/0.9.1 初等函数的积分.md"]
---

# 表 0.39 中 arcsin 行的被积函数与实数范围疑误

## 观察

表 0.39「基本积分」中，被积函数 $\frac{1}{a^{2}-x^{2}}$（$a>0$）出现了两次，对应两个不同的原函数：

| 函数 $f(x)$ | 不定积分 | 对实数的取值范围 |
|---|---|---|
| $\frac{1}{a^{2}-x^{2}}\,(a>0)$ | $\frac{1}{2a}\ln\left\|\frac{a + x}{a - x}\right\|$ | $x \neq a$ |
| $\frac{1}{a^{2}-x^{2}}\,(a>0)$ | $\arcsin \frac{x}{a}$ | $\|x\| < a$ |

第二行给出的原函数 $\arcsin \frac{x}{a}$ 的导数并不等于 $\frac{1}{a^{2}-x^{2}}$。

## 推理

由 $\frac{\mathrm{d}}{\mathrm{d}x}\arcsin \frac{x}{a} = \frac{1}{\sqrt{a^{2}-x^{2}}}$ 可知，与 $\arcsin \frac{x}{a}$ 相匹配的被积函数应为

$$
\frac{1}{\sqrt{a^{2}-x^{2}}}, \quad a>0,
$$

而实数条件 $|x| < a$ 也正好是该根式为正、反正弦有定义的条件。表中该行被积函数缺少根号，应为排版或转写时的脱漏。作为对照，表中相邻的 $\frac{1}{\sqrt{a^{2}+x^{2}}} \to \operatorname{arsinh}\frac{x}{a}$ 与 $\frac{1}{\sqrt{x^{2}-a^{2}}} \to \operatorname{arcosh}\frac{x}{a}$ 两行都带有根号。

## 直接证据与推断的区分

- **直接证据**：表中原样写作 $\frac{1}{a^{2}-x^{2}} \to \arcsin \frac{x}{a}$，且实数范围为 $|x| < a$。
- **推断**：该行被积函数应为 $\frac{1}{\sqrt{a^{2}-x^{2}}}$，据导数公式与实数范围 $|x| < a$ 的一致性得出。

## 相关页面

- 表的完整转录见 [[sources/10-数学指南实用数学手册--11-091-初等函数的积分--1xupt5l]]。
- 表中其他空缺与疑点见 [[queries/表039中复数取值范围空缺的含义]]。
