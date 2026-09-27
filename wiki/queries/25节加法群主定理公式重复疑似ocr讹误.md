---
type: query
title: 2.5 节加法群主定理公式中重复的 G_r 疑似 OCR 讹误？
created: 2026-09-27
updated: 2026-09-27
tags: [群论, 讹误, ocr]
related: [concepts/加法群的主定理, findings/加法群主定理与贝蒂数]
sources: ["数学指南_实用数学手册/2.5 代数结构.md"]
---

# 2.5 节加法群主定理公式中重复的 G_r 疑似 OCR 讹误？

## 问题

源文 2.5.1.3 "加法群的主定理"中的直和分解写作：

$$
G = G_1 \oplus G_2 \oplus \dots \oplus G_r \oplus G_r \oplus G_{r+1} \oplus \dots \oplus G_{r+s}.
$$

其中 $G_r$ 出现两次，与后续说明（$G_1,\dots,G_r$ 同构于 $\mathbb{Z}$；$G_{r+1},\dots,G_{r+s}$ 为有限阶循环群）不一致。

## 判断

疑为 OCR 重复，正确形式应为 $G_1\oplus\dots\oplus G_r\oplus G_{r+1}\oplus\dots\oplus G_{r+s}$。

## 同类疑点

源文 2.5.1.1 加法群定义 (i) 写作 $g+(h+k)=(g+h)+h$，末项应为 $+k$，亦疑为 OCR 讹误。

## 待办

- 核对纸质版原文，确认直和公式下标范围。

## Related
- [[queries/25节正规子群定义g范围疑似讹误]]
