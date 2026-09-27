---
type: query
title: Mathematica 求解部分分式分解仅一句话说明？
created: 2026-09-27
updated: 2026-09-27
tags: [mathematica, partial-fraction, open-question, source-gap]
related: [Mathematica, 部分分式分解, 214节Mathematica脚注内容缺失]
sources: ["数学指南_实用数学手册/2.1.7 部分分式分解.md"]
---

# Mathematica 求解部分分式分解仅一句话说明？

## 问题

2.1.7 节末以「用 Mathematica 求部分分式分解」为小标题，正文仅有一句：

> 「这个软件包能够确定任何有理函数的部分分式分解。」

该句**未给出函数名**（如 `Apart`）、未给出调用语法、未给出计算示例，也**未标注脚注编号**。与之相邻的 2.1.4 节亦有类似情况——见 [[queries/214节Mathematica脚注内容缺失|2.1.4 节 Mathematica 脚注内容缺失？]]。

## 待确认事项

1. 原书此处是否原本配有脚注或光盘/附录指引，而在当前来源中缺失？
2. 该「软件包」指的就是 [[entities/Mathematica|Mathematica]]，还是另有指代？
3. 若补全，应给出哪个函数（历史上 Mathematica 中为 `Apart[expr, x]`）及其适用范围（例如是否覆盖复系数、是否只处理最低项情形）？

## 影响

对本节影响有限：部分分式分解的数学内容（定理、两种求系数方法、非最低项归约）均独立完整，不依赖该句。但作为工具指引，此处信息明显不足。

## 相关页面

- [[entities/Mathematica|Mathematica]]
- [[concepts/部分分式分解|部分分式分解]]
- [[sources/10-数学指南实用数学手册--10-217-部分分式分解--7nbd0j|来源：2.1.7 部分分式分解]]