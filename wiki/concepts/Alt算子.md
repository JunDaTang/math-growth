---
type: concept
title: Alt 算子
created: 2026-09-27
updated: 2026-09-27
tags: [算子, 外代数, 三维向量, 闵可夫斯基几何]
related: [闵可夫斯基空间M4, 发散量算子Div, 霍奇星算子]
sources: ["数学指南_实用数学手册/3.9.4 闵可夫斯基几何.md"]
---

# Alt 算子

《数学指南》3.9.4 节对向量 $B=B^1e_1+B^2e_2+B^3e_3$ 定义算子

$$
\operatorname{Alt} (\boldsymbol {B}) := B ^ {1} \left(\boldsymbol {e} _ {2} \wedge \boldsymbol {e} _ {3}\right) + B ^ {2} \left(\boldsymbol {e} _ {3} \wedge \boldsymbol {e} _ {1}\right) + B ^ {3} \left(\boldsymbol {e} _ {1} \wedge \boldsymbol {e} _ {2}\right).
$$

## 说明

$\operatorname{Alt}$ 把空间部分（由 $e_1,e_2,e_3$ 张成的三维向量 $B$）映射为三个楔积 $e_2\wedge e_3$、$e_3\wedge e_1$、$e_1\wedge e_2$ 的线性组合，即映射到外代数中的 2 形式方向。

这一构造与三维空间中通常的向量积相对应：正文指出，外积 $u\wedge v=u\otimes v-v\otimes u$ 在三维情形下「对应于在三维空间中的通常向量积」。

## 关联

- 与 [[发散量算子Div]] 一起构成 3.9.4 节末尾的两个算子定义。
- 相关代数结构见外代数（格拉斯曼代数）与 [[霍奇星算子]]。