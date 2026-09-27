---
type: concept
title: z 截面（D_z）
created: 2026-09-27
updated: 2026-09-27
tags: [卡瓦列里原理, 截面, 累次积分, 几何]
related: [卡瓦列里原理-富比尼定理, 累次积分, 容许区域, 卡瓦列里原理由富比尼定理经平凡扩张推出]
sources: ["数学指南_实用数学手册/1.7.4 卡瓦列里原理(累次积分).md"]
---

# z 截面（D_z）

## 定义

在 1.7.4 节中，区域 $D \subseteq \mathbb{R}^N$ 的 **$z$ 截面**定义为

```latex
D_{z} := \{\boldsymbol{y} \in \mathbb{R}^{K} : (\boldsymbol{y}, \boldsymbol{z}) \in D\}
```

其中 $\mathbb{R}^N = \mathbb{R}^K \times \mathbb{R}^M$，点写作 $(\boldsymbol{y}, \boldsymbol{z})$。

直观地说：固定外层变量 $\boldsymbol{z}$，把区域 $D$ 沿 $\boldsymbol{z}$ 方向「切」出来的那个 $\mathbb{R}^K$ 子集就是 $D_z$。

## 作用

$z$ 截面是 [[concepts/卡瓦列里原理-富比尼定理]]（公式 1.141）中累次积分的**内层积分域**：外层对 $\boldsymbol{z} \in \mathbb{R}^M$ 积分，内层在截面 $D_z$ 上对 $\boldsymbol{y}$ 积分，从而把 $D$ 上的积分化为累次积分。

在 1.7.4 节的原文中，公式 (1.141) 的内层写作 $\int_{D} f_*(\boldsymbol{y},\boldsymbol{z})\,\mathrm{d}\boldsymbol{y}$（对被积函数做平凡扩张），$D_z$ 则是与之配套的几何描述。

## 源文措辞说明

源文写作「$D$ 的 $z$ 截面 $D_z$ **如上定义**」，表明该记号应在更早处（1.7.1／1.7.2 附近）已引入，但在 1.7.4 节的录入文本中没有给出定义行。跨子节核对可确认其首次出现位置。