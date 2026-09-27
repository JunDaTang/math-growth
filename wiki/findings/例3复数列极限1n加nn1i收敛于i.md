---
type: finding
title: 例 3：复数列 1/n + n/(n+1)i 收敛于 i
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 复变函数, 复数列, 算例]
related: [复数列, 复数列收敛等价于实部虚部分别收敛]
sources: ["数学指南_实用数学手册/1.14.2 复数列.md"]
source: "[[10-数学指南实用数学手册--8-1142-复数列--1imd07l]]"
confidence: high
replicated: null
---

# 例 3：复数列 $1/n + \frac{n}{n+1}\mathrm{i}$ 收敛于 $\mathrm{i}$

## 题目

求复数列 $\left(\frac{1}{n} + \frac{n}{n+1}\mathrm{i}\right)$ 当 $n \to \infty$ 时的极限。

## 解答

由于当 $n \to \infty$ 时 $1/n \to 0$，$n/(n+1) \to 1$，因而

$$
\lim_{n \to \infty} \left(\frac{1}{n} + \frac{n}{n+1}\mathrm{i}\right) = \mathrm{i}.
$$

## 说明

该例示范了 [[复数列收敛等价于实部虚部分别收敛]] 的用法：分别计算实部 $1/n \to 0$ 与虚部 $n/(n+1) \to 1$，即得极限的实部为 $0$、虚部为 $1$，故极限为 $\mathrm{i}$。

## 相关来源

《数学指南——实用数学手册》1.14.2 节例 3（见 [[10-数学指南实用数学手册--8-1142-复数列--1imd07l]]）。
