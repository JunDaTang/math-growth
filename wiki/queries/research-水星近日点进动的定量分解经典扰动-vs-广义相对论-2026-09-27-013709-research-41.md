---
type: query
title: "Research: 水星近日点进动的定量分解：经典扰动 vs 广义相对论"
created: 2026-09-27
origin: deep-research
tags: [research]
---

# Research: 水星近日点进动的定量分解：经典扰动 vs 广义相对论

# 水星近日点进动的定量分解：经典扰动 vs 广义相对论

## 概述

水星近日点进动（perihelion precession of Mercury）是广义相对论最早、也最经典的观测检验之一。对其观测值的定量分解通常表述为：**总进动 ≈ 其他行星的牛顿引力扰动 + 太阳扁率（四极矩）+ 广义相对论（后牛顿）修正 + 极小的参考系拖曳项**。其中经典牛顿扰动解释了绝大部分进动，而剩余约 43″/世纪（arcseconds per century）的"反常进动"正是 [[扰动理论与广义相对论]] 中广义相对论所预言的贡献，也是 [[爱因斯坦]] 1915 年理论的首次定量胜利。

本页以 [[水星近日点进动]] 为问题线索，整理各来源给出的数值、公式、历史与争议。

---

## 一、观测总量：必须先区分两种参考系

在讨论"分解"之前，必须区分两个常被混淆的总量：

1. **相对惯性参考系（ICRF）的进动**：约 **(574.10 ± 0.65)″/世纪** [2]，文献中常简写为 574″/世纪 [3][4]。
2. **从地球上看去的进动**：约 **5599.7″/世纪** 或 **5600″/世纪** [5][9]。这一较大的数值包含了地球自身的**岁差**（约 **5025″/世纪**）[1]。

换言之：

> 5600″（地球视角） − 5025″（地球岁差） ≈ 575″（惯性系总进动）[1]

因此，所谓"水星的 43″ 反常进动"，指的是扣除地球岁差与所有牛顿扰动后、在惯性系中剩余的进动量。不同文献在总量上出现 574″、575″、5600″ 等差异，根源在于**参考系与时间单位（Julian century vs. tropical century）的选择**，而非物理分歧。

---

## 二、核心分解表

下表以 Wikipedia《Tests of general relativity》给出的、相对 ICRF 的分解为准 [2]：

| 数值（″/Julian century） | 成因 |
| --- | --- |
| 532.3035 | 其他太阳系天体的引力牵引（牛顿扰动） |
| 0.0286 | 太阳扁率（四极矩） |
| 42.9799 | gravitoelectric 效应（类 Schwarzschild），即广义相对论效应 |
| −0.0020 | Lense–Thirring（参考系拖曳）进动 |
| **575.31** | **理论预言总计** |
| **574.10 ± 0.65** | **观测值** |

其中广义相对论修正项 **(42.980 ± 0.001)″/世纪** 的参数设定为后牛顿参数 **γ = β = 1** [2]。这表明该残余进动可被广义相对论完全解释，而基于更精确测量的近期计算并未实质改变这一结论 [2]。

另有来源给出的近似分解（取整数）为 [3][4]：

```
水星近日点进动总量:              574″/世纪
其他行星的牛顿扰动:              531″/世纪
广义相对论修正:                   43″/世纪
Dicke 太阳扁率的牛顿修正:          3″/世纪
```

两套数字的差异主要来自太阳扁率项与四舍五入：Wikipedia 表把太阳扁率单列（0.0286″），而 [3][4] 引述的是 Dicke–Goldenberg 所主张的较大扁率（约 3″）。

---

## 三、经典（牛顿）扰动的贡献

- **其他行星的引力牵引**：约 **531″/世纪** [3][4][6][7]，更精确值为 **532.3035″/世纪** [2]。这是水星总进动中数值最大的单项。
- **太阳扁率（四极矩）**：标准太阳模型给出的小量约 **0.0286″/世纪** [2]。历史上 Dicke 与 Goldenberg 曾宣称观测到远大于模型预言的太阳扁率，对应牛顿修正约 **3″/世纪**，这一度威胁到广义相对论与观测的吻合 [3][4]（详见第六节）。
- 单位换算上，牛顿扰动约合每个轨道周期 **1.28″**，而总进动约 **1.38″/轨道**，二者之差约 **0.10″/轨道** 即为广义相对论所解释的部分 [8]。

结论：**在牛顿框架内，经典扰动无法解释约 43″/世纪 的剩余进动**，这一结论经 160 余年的长期计算被普遍接受 [1]。

---

## 四、广义相对论的贡献

### 数量级

- 每个轨道周期约 **0.10″** [1][8]，约合 **5.21 × 10⁻⁷ 弧度/ revolution** [1]。
- 每年约 **0.41″–0.43″** [10][13]。
- 每世纪约 **42.98″–43″**（取 γ = β = 1）[2][12]。

### 解析公式

广义相对论对牛顿引力的修正可写为对单位质量受力的小修正 [10][13]，由此得到每转的近日点前移为

$$\Delta\phi \approx \frac{6\pi G M}{c^2\, a\,(1-e^2)} \quad (\text{radians per revolution})$$

更一般的**参数化后牛顿（PPN）**形式为：半通径为 $L$ 的轨道每转进动等于

$$\frac{6\pi m}{L} \times \frac{2 - \beta + 2\gamma}{3}$$

由于观测到的水星进动与 $6\pi m/L$ 高度吻合，且 γ 可由其他手段独立测定为 1，因此可反推 **β = 1**，与 Einstein 场方程一致；这也是广义相对论最强有力的验证之一 [12]。

### 对其他行星的推广

同样公式对金星给出约 **8.6″/世纪** 的残余进动——数值远小于水星，原因是金星离太阳更远、该处时空曲率更小 [5]。对其他行星的广义相对论贡献则基本可忽略 [10][13]。

---

## 五、历史脉络

- **1859 年**：[[勒维耶]]（Urbain Le Verrier）重新分析 1697–1848 年间水星凌日观测，首次发现实际进动与牛顿理论预言存在偏差，原始偏差值为 **38″/tropical century** [1][2]。他称此为"一个重要的天文学问题" [1]。
- **19 世纪下半叶**：勒维耶提出可能存在一颗尚未发现的"扰动行星"来解释这一偏差，该假想行星被命名为 **Vulcan（火神星）** [1][2]。类似的 ad hoc 方案（如太阳与水星之间存在尘埃）均因与其他观测矛盾而失败 [5]。
- **1882 年**：Simon Newcomb 将偏差修正为 **43″/tropical century** [1][2][6][9]。
- **1915 年 11 月 18 日**：Einstein 在最终场方程完成前不久，基于真空场方程给出水星进动的推导，结果在最终理论中保持不变 [12]。据记载，Einstein 在确认理论与观测吻合后兴奋了数日 [12]。
- 这一"反常进动"的解决成为 [[爱因斯坦]] 广义相对论被广泛接受的关键推动因素 [2]。

---

## 六、单位换算与常见混淆

- **角秒与轨道计数**：水星每世纪约绕日 **415 次**，故 0.10″ × 415 ≈ 41–42″，与 Newcomb 的值吻合 [8]。这解释了"0.10″/轨道"与"38–43″/世纪"其实是同一件事的不同单位表达 [8]。
- **Julian century vs. tropical century**：不同来源分别使用两者，数值略有差异（如 42.9799″/Julian century [2] vs. 43″/tropical century [1]）。
- **"从地球看" vs. "惯性系"**：见第一节。
- 注意：0.10″/轨道所对应的总进动是 1.38″/轨道，不是全部由 GR 贡献；GR 只占其中约 0.10″ [8]。

---

## 七、争议、未决问题与矛盾

1. **Dicke–Goldenberg 太阳扁率问题**：他们声称探测到远大于太阳模型预言的太阳扁率，其尺寸"大到足以破坏 GR 与水星轨道的吻合，却又不足以支持牛顿解释" [3][4]。数值上对应约 3″/世纪的牛顿修正 [3][4]。标准模型中该量仅约 0.0286″/世纪 [2]，后续研究倾向支持标准模型，但这一插曲至今仍被作为"GR 检验的边界条件"提及。

2. **Will 2018 的新 GR 项**：Clifford Will 于 2018 年在 *Physical Review Letters* 发表新计算，考虑太阳系各行星对水星进动的影响，得到对标准 43″/世纪 预言的进一步 GR 修正（量级为百万分之几），并指出该效应可能由 **Bepi Colombo** 任务测量 [3]。

3. **关于 Einstein 1915 年原稿的争议**：有论文（scirea.org）声称 Einstein 计算水星近日点的原始论文存在**四处错误**——积分错误（若无误则进动应为 71.7″/世纪 [11]）、积分函数展开系数错误（若无误应为 14.3″/世纪 [11]）、把椭圆轨道的近日点与远日点当作被积函数展开的极点（导致 GR 修正项为零）、以及假设公式中的常数项等于牛顿引力公式中的常数项。该文作者据此认为"广义相对论只能描述太阳系行星的（带小修正的）抛物线轨道，无法描述椭圆与双曲线轨道" [11]。**这是一个边缘性主张**，与主流广义相对论界（如 [2][12]）的结论相冲突；主流工作表明标准推导在 β = γ = 1 下给出 42.98″/世纪，且与观测高度吻合 [2][12]。

4. **来源 [1] 的表述矛盾**：该文以 Eq.(30) 计算得 5.21×10⁻⁷ rad/rev（≈ 0.107″）与 44.39″/tropical century，却将其称为"牛顿引力对水星近日点进动的贡献"，并称其"良好近似观测值 43″ 及广义相对论的 42.98″" [1]。这一措辞把 GR 特有的数值量纲（0.10″/轨道级）冠以"牛顿贡献"之名，与主流文献中牛顿扰动约 531″/世纪 的结论明显冲突 [2][3][4]。**应谨慎对待该文的术语与结论**，其计算数值本身与 GR 预言一致，但归因类别存疑。

5. **观测数据的精度限制**：目前观测值 (574.10 ± 0.65)″/世纪 与理论总计 575.31″/世纪 存在约 1.2″ 的差距，部分处在观测误差范围内 [2]，新测量尚未实质改变这一局面 [2]。

---

## 八、建议补充来源

为完善本页，建议进一步检索：

- Clifford Will, *Was Einstein Right? Putting General Relativity to the Test*（1986）及 2018 年 *PRL* 新论文的原文本，以核实 D 项与 Bepi Colombo 可测性主张 [3]。
- IAU / NASA JPL 关于水星进动的官方数值与误差分析，以统一 Julian/tropical century 的换算口径。
- Lense–Thirring 进动（−0.0020″/世纪 [2]）的原始推导文献，以评估该极小项在现代观测中的可分辨性。
- PPN 形式中 β、γ 的联合约束文献，补充"仅凭水星如何定出 β = 1"的推导细节 [12]。
- 关于太阳四极矩 J₂ 的最新日震学测定，以判定 Dicke–Goldenberg 主张的最终归属 [3][4]。

---

## 相关页面

- [[水星近日点进动]]
- [[扰动理论与广义相对论]]
- [[爱因斯坦]]
- [[勒维耶]]
- [[牛顿]]
- [[万有引力定律]]
- [[开普勒三定律]]
- [[行星运动微分方程]]
- [[行星运动的数学描述]]
- [[初等数学公式的历史代价]]

## References

1. [Precession of planets' orbits between Newtonian gravity and Einstein's general relativity - Top Italian Scientists Journal](https://journal.topitalianscientists.org/Precession_of_planets_orbits_between_Newtonian_gravity_and_Einstein_s_general_relativity) — journal.topitalianscientists.org
2. [Tests of general relativity](https://en.wikipedia.org/wiki/Tests_of_general_relativity) — en.wikipedia.org
3. [GR and Mercury's Orbital Precession](https://math.ucr.edu/home/baez/physics/Relativity/GR/mercury_orbit.html) — math.ucr.edu
4. [GR and Mercury's Orbital Precession](https://www.desy.de/user/projects/Physics/Relativity/GR/mercury_orbit.html) — desy.de
5. [Precession of the perihelion of Mercury](https://aether.lbl.gov/www/classes/p10/gr/PrecessionperihelionMercury.htm) — aether.lbl.gov
6. [Newton's Methodology and Mercury's Perihelion Before ...](https://www.jstor.org/stable/10.1086/525634) — jstor.org
7. [Newtonian contribution to perihelion precession of Mercury](https://physics.stackexchange.com/questions/696607/newtonian-contribution-to-perihelion-precession-of-mercury) — physics.stackexchange.com
8. [Instagram](https://www.instagram.com/reel/Db3S7ioC2lh) — instagram.com
9. [Compact calculation of the Perihelion Precession of ...](https://arxiv.org/pdf/astro-ph/0305181) — arxiv.org
10. [Perihelion precession of Mercury](https://farside.ph.utexas.edu/teaching/celestial/Celestial/node45.html) — farside.ph.utexas.edu
11. [Four Mistakes in the Original Paper of Einstein in 1915 to Calculate the Precession of Mercury’s Perihelion](https://www.scirea.org/journal/PaperInformation?PaperID=7180) — scirea.org
12. [Conquering the Perihelion](https://www.mathpages.com/rr/s8-10/8-10.htm) — mathpages.com
13. [Perihelion Precession of Mercury](https://farside.ph.utexas.edu/teaching/336k/Newton/node116.html) — farside.ph.utexas.edu
