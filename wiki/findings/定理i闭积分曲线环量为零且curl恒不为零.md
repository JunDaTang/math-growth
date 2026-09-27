---
type: finding
title: 定理 (i)：闭积分曲线处环量为零且 curl v 恒不为零
source: "[[10-数学指南实用数学手册--20-198-环量闭积分曲线与斯托克斯积分定理--gv2pcd]]"
confidence: medium
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [向量分析, 环量, 闭积分曲线, 旋度]
related: [闭积分曲线, 环量, 旋度, 斯托克斯积分定理]
sources: ["数学指南_实用数学手册/1.9.8 环量、闭积分曲线与斯托克斯积分定理.md"]
---

# 定理 (i)：闭积分曲线处环量为零且 curl v 恒不为零

1.9.8 的定理 (i)（原文逐字引述）：

> 定理 (i) 如果 $\partial M$ 是闭积分曲线, 则沿 $\partial M$ 的环量为零, 且 $\operatorname{curl} v$ 在 $D$ 上恒不为零.

## 内容拆解

该定理包含两个断言：

1. 若边界 $\partial M$ 本身是向量场 $\boldsymbol{v}$ 的[[concepts/闭积分曲线]]，则沿 $\partial M$ 的[[concepts/环量]]为零；
2. 此时 $\operatorname{curl} \boldsymbol{v}$ 在区域 $D$ 上恒不为零（处处不等于零向量）。

## 证据等级与问题

- 教材陈述型结果，**本节未给证明与出处**。
- `confidence: medium` 的原因：定理措辞中的区域记号 $D$ 在 1.9.8 前后文未加定义（本节讨论的是曲面 $M$ 与其边界 $\partial M$），指代关系不明，见 [[queries/198节定理i中D与M指代不一致]]。
- 第二断言与定理 (ii) 的方向相反（见 [[findings/定理ii curl恒为零则不存在闭积分曲线]]），两条断言之间的关系需要证明才能确认。

## 相关页面

[[concepts/闭积分曲线]]、[[concepts/环量]]、[[concepts/旋度]]、[[concepts/斯托克斯积分定理]]。