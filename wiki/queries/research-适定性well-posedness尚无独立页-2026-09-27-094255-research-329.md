---
type: query
title: "Research: 适定性（well-posedness）尚无独立页"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 适定性（well-posedness）尚无独立页

# 适定性（well-posedness）

适定性（well-posedness，又译「良定性」）是刻画一个数学「问题」是否具有良好结构的基本概念。按 Hadamard 的经典表述，一个问题若同时满足若干条件（通常为存在性、唯一性与解对数据的连续依赖性），则称为**适定的**；否则称为**不适定的**（ill-posed）。这一概念横跨偏微分方程、常微分方程、随机分析、优化理论、博弈论乃至社会科学的方法论，是各部分研究中反复出现的核心判据。[2][5][11]

## Hadamard 准则

Hadamard 的原始表述针对 Cauchy 问题（初值问题），其标准形式通常包含三条：[2][4][5][11]

1. **存在性（existence）**——问题至少有一个解；
2. **唯一性（uniqueness）**——解是唯一的；
3. **连续依赖性（continuous dependence / stability）**——解连续地依赖于给定的数据（初值、边界条件、方程系数等）。

同时满足这三条的问题称为「在 Hadamard 意义下适定」（well-posed in the Hadamard sense）。文献 [11] 将这一准则表述为 Definition 1（Well-Posed Problem），并强调其最初是为偏微分方程的 Cauchy 问题而提出的，后被推广为一种方法论上的「认识论护栏」（epistemic guardrails）。[11]

需注意，某些文献在三条之外还附加要求（例如解须属于某一指定的函数空间），因此「适定性」的具体定义在不同语境下并不完全统一。[1][5]

## 偏微分方程中的适定性

### Hadamard 局部适定性

偏微分方程文献中最常见的短语是 **Hadamard local well-posedness（Hadamard 局部适定性）**，其含义即把上述三条限制在局部时间区间上，并常在 Sobolev 空间 H^s 中建立理论。典型例子包括：

- **带超临界源项与阻尼的非线性波动方程**：[1] 研究了该系统（PDE 系统 (1)）弱解的 Hadamard 适定性，并与半线性波动方程解的适定性问题相联系。
- **不可压缩自由边界 Euler 方程**：[2] 给出了 H^s 空间中一套完整的局部适定理论，明确包括 (i) Hadamard 意义下的局部适定性，即局部存在性、唯一性……
- **自由边界相对论 Euler 方程（物理真空边界）**：[4] 同样给出完整的局部适定理论，并扩展至粗糙解与延拓判据（continuation criterion）。
- **有限区间上的高阶非线性 Schrödinger 方程**：[3] 建立了某类三阶非线性方程的局部 Hadamard 适定性，证明了唯一解的存在性以及解对数据的连续依赖性。
- **非线性发展方程**：[5] 在 Hadamard 经典意义下讨论了若干类非线性偏微分方程 Cauchy 问题的适定性，并区分「条件适定」与「无条件适定」（conditional and unconditional well-posedness）。

在这些工作中，适定性的证明往往同时给出**唯一性**与**对数据的连续依赖**，并进而研究**延拓判据**（即解在何时可继续延拓）与**粗糙解**（rough solutions）等加强结论。[2][4]

### 边值问题、随机与反应扩散方程

- **四阶常微分方程三点边值问题**：[6] 研究其正解的**存在性、唯一性**，并借助数值模拟呈现结果，指出既有文献多限于两点边值条件。
- **随机微分方程**：[7] 对若干具体随机微分方程证明解的**存在性与唯一性**，并指出证明过程中 **Lipschitz 条件必不可少**。
- **反应扩散方程行波解**：[8] 综述了行波解的**存在性与唯一性**以及在一定条件下的**稳定性与渐近行为**，方法涉及比较原理、加权能量法、挤压技术（squeezing）等。
- **具有混合边界条件的非线性黏弹性波方程**：[9] 研究其解的**适定性**，综合运用经典 Galerkin 逼近方法与紧性定理证明**正则解的存在唯一性**。
- **弹性力学中的唯一性定理**：[10] 明确把弹性力学问题的**适定性**界定为「存在性、唯一性以及稳定性（对边界条件的连续依赖性）」。

上述诸例表明，中文文献常以「适定性」一词统摄「存在性 + 唯一性 + 稳定性」这组含义，与 Hadamard 三条准则一致。[9][10]

## 优化问题中的适定性：Tykhonov 与 Hadamard 两种概念

优化理论中的适定性有两条并行脉络，文献中常被对照讨论：[14][15]

- **Tykhonov（Tychonov）意义下的适定性**：若 f 在集合 K 上有唯一极小点，且每一个极小化序列都收敛到该极小点，则称 f 在 K 上按 Tychonov 意义适定。[15]
- **Hadamard 意义下的适定性**：除唯一解外，还要求问题对数据连续依赖（即数据扰动时解随之连续变化）。[12][15]

文献 [12] 给出 Definition 2.5：极小化问题 (A, I) 称为 **T-Hadamard well-posed**，当且仅当它有唯一解 X₀ ∈ A，且存在一列扰动问题 {(Aₙ, …)} 满足相应收敛条件。文献 [13] 在非合作博弈论中进一步区分：y 称为**广义 Hadamard 适定**（generalized Hadamard well-posed），若 F(y) 非……；而 y 称为 **Hadamard 适定**，若它具有（唯一的）……。专著 [14] 则同时研究 Tykhonov 与 Hadamard 两种适定性概念、二者的联系以及若干推广（例如放宽唯一性要求）。

## 在其他领域中的推广

- **博弈论**：[13] 把 Hadamard 适定性推广到**不连续非合作博弈**（discontinuous non-cooperative games）的情境。
- **社会科学**：[11] 提出把 Hadamard 的适定问题准则作为社会科学建模的「认识论护栏」，认为该准则有助于界定何为一个良定义的（well-posed）实证或理论问题。

## 与现有 wiki 的关联

现有 wiki 中虽无适定性的独立页面，但若干入库条目研究了「存在性—唯一性—稳定性」的问题结构，可作为本题的上下文：

- [[薄膜振动的初边值问题]] 与 [[单位圆盘上的狄利克雷特征值问题]]：典型的初边值问题，其唯一解由 [[傅里叶方法]] 给出；
- [[奇异微分方程]]、[[正则奇点]] 与 [[Frobenius幂级数解法]]：围绕正则奇点处解的存在性与解的形态展开；
- [[解析延拓]] 与 [[恒等原理]]：解析延拓的唯一性属于「唯一性」这一适定性要素的复分析对应物；
- [[狄利克雷]] 与 [[拉普拉斯]]：分别关联边值条件与 Laplace 算子，是适定性讨论中常见的边界与算子背景。

## 矛盾与空白

- **术语不统一**：「适定」的具体定义在不同领域（PDE、优化、博弈论、社会科学）有所差异；PDE 强调对数据的连续依赖，优化中则并置 Tykhonov 与 Hadamard 两种范式，且常放宽唯一性要求。[12][14][15]
- **中文译法**：「适定性」「良定性」「适定问题」等译名并存，中文文献与英文术语的对应关系并不严格。[6][9][10]
- **附加准则**：Hadamard 三准则之外是否应要求「解属于指定函数空间」等条件，文献间并未形成共识。[1][5]
- **原始出处缺失**：本批来源均转述 Hadamard 准则，未直接引用其原始讲演，历史脉络有待考订。[11][14]

## 建议补充来源

- Jacques Hadamard 关于偏微分方程物理意义的原始讲演（1902 年前后），以追溯准则的最初表述。
- Tikhonov（1966）关于稳定性与适定性的经典论文，以厘清 Tykhonov 适定性的源头。
- Dontchev 与 Zolezzi 的专著 *Well-Posed Optimization Problems*（对应来源 [14]），系统对照 Tykhonov 与 Hadamard 两种概念。
- 关于 Cauchy 问题不适定性的标准反例（如 Hadamard 的 Laplace 方程初值问题反例），以补足「不适定」一侧的论述。

## References

1. [Local Hadamard well-posedness for nonlinear wave equations with supercritical sources and damping](https://www.sciencedirect.com/science/article/pii/S002203961000094X) — sciencedirect.com
2. [Sharp Hadamard local well-posedness, enhanced uniqueness and pointwise continuation criterion for the incompressible free boundary Euler equations](https://link.springer.com/article/10.1007/s40818-025-00204-4) — link.springer.com
3. [Well-posedness of the higher-order nonlinear Schrödinger equation on a finite interval](https://link.springer.com/article/10.1007/s00028-025-01154-x) — link.springer.com
4. [The relativistic Euler equations with a physical vacuum boundary: Hadamard local well-posedness, rough solutions, and continuation criterion: Marcelo M. Disconzi …](https://link.springer.com/article/10.1007/s00205-022-01783-3) — link.springer.com
5. [Conditional and unconditional well-posedness for nonlinear evolution equations](https://projecteuclid.org/journals/advances-in-differential-equations/volume-9/issue-3-4/Conditional-and-unconditional-well-posedness-for-nonlinear-evolution-equations/ade/1355867944.full) — projecteuclid.org
6. [一类四阶常微分方程三点边值问题正解的存在性与稳定性分析研究](https://hndk.hainanu.edu.cn/article/cstr/32403.14.hndk.2024043001) — hndk.hainanu.edu.cn
7. [几种随机微分方程解的存在性与唯一性](https://www.hanspub.org/journal/paperinformation?paperID=14859) — hanspub.org
8. [关于反应扩散方程的行波解的存在唯一性与稳定性以及渐近行为的综述](https://pdf.hanspub.org/pm2024146_111252453.pdf) — pdf.hanspub.org
9. [具有混合边界条件的非线性波方程解的适定性研究](http://www.bnujournal.com/article/doi/10.12202/j.0476-0301.2025118) — bnujournal.com
10. [若干弹性力学问题解的唯一性定理](https://www.sciengine.com/parse/pdf/1674-7275/9F7C2EFFCB934E49B5F19ADF8D3DF110.pdf) — sciengine.com
11. [Toward Well-Posed Problems in the Social Sciences: Hadamard's Criteria as Epistemic Guardrails](https://arxiv.org/abs/2609.22321) — arxiv.org
12. [Various aspects of well-posedness of optimization problems](https://link.springer.com/content/pdf/10.1007/978-94-015-8472-2.pdf#page=232) — link.springer.com
13. [Hadamard well-posedness in discontinuous non-cooperative games](https://www.sciencedirect.com/science/article/pii/S0022247X09005721) — sciencedirect.com
14. [Well-posed optimization problems](https://books.google.com/books?hl=en&lr=&id=WG96CwAAQBAJ&oi=fnd&pg=PA1&dq=Hadamard+well-posed+problem+definition&ots=1QyvWh5fUX&sig=dYceikglwbG3We0Em6DAHDk5WIc) — books.google.com
15. [Hadamard and Tyhonov well-posedness of a certain class of convex functions](https://www.sciencedirect.com/science/article/pii/0022247X82901871) — sciencedirect.com

## Related
- [[queries/research-能量方法与最大值原理的适用范围为何互补-2026-09-27-094356-research-330]]
- [[queries/research-热核与磨光效应作为独立条目-2026-09-27-092518-research-321]]
- [[queries/research-术语映射度与拓扑度brouwer-degree的区分与联系-2026-09-27-100021-research-341]]
