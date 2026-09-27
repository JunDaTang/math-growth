---
type: finding
title: 极坐标面积元为 r dr dφ
source: "[[10-数学指南实用数学手册--8-171-基本思想--14h73zm]]"
confidence: high
replicated: null
created: 2026-09-27
updated: 2026-09-27
tags: [数学, 微积分, 极坐标, 多变量积分]
related: [极坐标下的二重积分, 多变量积分代换公式, 雅可比行列式, 极坐标变换]
sources: ["数学指南_实用数学手册/1.7.1 基本思想.md"]
---

# 极坐标面积元为 r dr dφ

## 论断

在变换 $x = r\cos\varphi$、$y = r\sin\varphi$（$-\pi < \varphi \leqslant \pi$）下，

$$
\int_{D}\varrho(x,y)\,\mathrm{d}x\,\mathrm{d}y = \int_{D'}\varrho\, r\,\mathrm{d}r\,\mathrm{d}\varphi, \tag{1.132}
$$

其依据是雅可比行列式

$$
\frac{\partial(x,y)}{\partial(r,\varphi)} = \begin{vmatrix} \cos\varphi & -r\sin\varphi \\ \sin\varphi & r\cos\varphi \end{vmatrix} = r(\cos^{2}\varphi + \sin^{2}\varphi) = r.
$$

## 两重证据

1. **代数推导**：由代换公式 (1.131) 直接计算行列式，结果为 $r$（在 $r > 0$ 处满足正性条件）。
2. **几何直观**（来源脚注 1）：把区域分割成小片 $\Delta F = r\Delta r\Delta\varphi$，对和 $\sum \varrho r\Delta r\Delta\varphi$ 取极限 $\Delta F \to 0$。

两种论证相互印证，且 $r$ 因子恰好解释了为何二维幂函数积分 $\int \mathrm{d}x\,\mathrm{d}y / r^{\alpha}$ 的收敛阈值出现在 $\alpha = 2$（见 [[无界区域上的二重积分]] 与 [[无界函数的二重积分]]）。

## 相关页面

- [[极坐标下的二重积分]]、[[多变量积分代换公式]]、[[雅可比行列式]]、[[极坐标变换]]
