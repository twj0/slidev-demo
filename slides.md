---
theme: seriph
background: https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop
title: 氢气制取技术：产业与学术前沿
info: |
  ## 氢气制取技术：产业与学术前沿
  面向可再生能源概论课程
class: text-center text-slate-100
colorSchema: dark
highlighter: shiki
drawings:
  persist: false
transition: view-transition
css: unocss
mdc: true
---

<div class="pointer-events-none fixed inset-0 -z-10 bg-gradient-to-br from-slate-950 via-slate-900 to-black"></div>
<div class="pointer-events-none fixed -top-40 -right-24 h-72 w-72 bg-sky-500/40 blur-3xl rounded-full mix-blend-screen animate-pulse"></div>
<div class="pointer-events-none fixed -bottom-40 -left-24 h-72 w-72 bg-emerald-400/30 blur-3xl rounded-full mix-blend-screen animate-pulse"></div>

# 氢气制取技术：产业与学术前沿

<div class="text-2xl opacity-90 mt-4 text-slate-100 drop-shadow-xl tracking-wide">
面向可再生能源概论课程
</div>

<div class="abs-br m-6 flex gap-2 text-slate-300">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

---
layout: image-right
image: https://images.unsplash.com/photo-1473341304170-971dccb5ac1e?q=80&w=2070&auto=format&fit=crop
transition: slide-left
---

# 为什么关注氢能？

<v-clicks>

- **脱碳需求**: 解决钢铁、化工、重卡等"难减排"领域的碳排放。
- **能源载体**: 链接电力系统与化工/交通系统的纽带。
- **长时储能**: 解决可再生能源（风、光）的季节性波动。

</v-clicks>

<br>

<div v-click class="bg-green-500/10 p-4 rounded-lg border-l-4 border-green-500">
  <span class="font-bold">核心驱动力：</span> 全球已有 40+ 国家发布国家氢能战略。
</div>


---
layout: image-right
image: https://www.researchgate.net/publication/351301827/figure/fig1/AS:1024814378668035@1621346196464/Water-electrolysis-principle-Two-electrodes-are-placed-in-the-electrolyte-solution.png
transition: slide-left
topic: intro
class: text-left
---

# 电解水制氢：通往绿氢的主干道

<v-clicks>

- **基本原理**：$2H_2O \rightarrow 2H_2 + O_2$，实际运行电压通常 1.8–2.2 V。  
- **主要路线**：低温 ALK / PEM / AEM 与高温 SOEC 两大类，可通过选择工艺在效率与成本之间权衡。  
- **与风光耦合**：要求制氢系统具备宽负荷、快速启停能力，PEM/AEM 更适配高波动、快速调节场景。  
- **能耗与效率示例**：以 2.0 V 运行时，1 kg H₂ 约需 53–55 kWh 电能，对应电解效率约 60–65%。  

</v-clicks>

---
layout: center
topic: intro
transition: slide-up
---

# 核心技术路线对比 (2025)

| 特性 | 碱性电解 (ALK) | 质子交换膜 (PEM) | 阴离子交换膜 (AEM) |
| :--- | :---: | :---: | :---: |
| **成熟度 (TRL)** | **9 (成熟)** | **8-9 (商业化)** | 6-7 (示范) |
| **电流密度** | 0.4-0.6 A/cm² | **2.0-3.0 A/cm²** | 1.0-2.0 A/cm² |
| **动态响应** | 分钟级 | **毫秒级** | 秒级 |
| **关键材料** | 镍, 不锈钢 | **铂, 铱 (贵金属)** | 镍, 铁 (非贵金属) |
| **CAPEX ($/kW)** | **300-600** | 800-1200 | 400-600 (潜力) |
| **适用场景** | 稳态大规模制氢 | 波动性风光耦合 | 分布式/低成本潜力 |

<div class="mt-6 text-xs opacity-60 text-center">
  数据来源: IEA Global Hydrogen Review 2025, IRENA [1][2]
</div>

---
layout: two-cols
topic: alk
transition: slide-left
---

# 碱性电解水 (ALK)
**工作原理**

<v-clicks>

- **电解质**: 30% KOH 溶液 (强碱性)。
- **隔膜**: 多孔隔膜 (Diaphragm)，允许 OH⁻ 通过，阻隔气体。
- **电极**: 镍基催化剂 (Ni, Ni-Mo 等)。
- **反应**:
  - 阴极: $2H_2O + 2e^- \rightarrow H_2 + 2OH^-$
  - 阳极: $2OH^- \rightarrow 1/2O_2 + H_2O + 2e^-$

</v-clicks>

::right::

<div class="ml-4 mt-8">
  <img 
    v-motion
    :initial="{ opacity: 0, y: 50 }"
    :enter="{ opacity: 1, y: 0, transition: { duration: 800 } }"
    src="https://ars.els-cdn.com/content/image/1-s2.0-S2352484722020625-gr3.jpg" 
    class="rounded-lg shadow-lg border border-gray-500/20"
  />
  <div class="text-center text-xs opacity-50 mt-2">ALK 离子传输机制</div>
</div>

---
layout: image-left
image: https://nickelgreen.com/wp-content/uploads/2024/01/AWE-hydrogen-production.jpg
topic: alk
transition: slide-left
---

# ALK 的规模化之路

**中国供应链的统治力**

<v-clicks>

- **单槽规模**: 从 5 MW 迈向 **10-20 MW** (2025 主流)。
- **产氢量**: 单体可达 **2000-4000 Nm³/h**，系统效率提升至 60-70%。
- **成本优势**: 中国供应链主导 (61% 产能)，CAPEX 低至 **$300/kW** (欧美 $800/kW) [11]。
- **技术迭代**: 
  - **零极距 (Zero-gap)**: 降低欧姆损耗。
  - **Zirfon 隔膜**: 气密性与离子传导率的双重提升 [17]。

</v-clicks>

<br>

<div v-click class="bg-orange-500/10 p-3 rounded text-sm">
  ⚠️ <b>挑战:</b> 动态响应较慢，冷启动时间长，难以完美跟随风光剧烈波动。
</div>

---
layout: two-cols
topic: pem
transition: slide-left
background: https://www.researchgate.net/publication/339946556/figure/fig1/AS:869574543147008@1584334135629/Experimental-setup-the-high-pressure-characterization-of-PEM-electrolyzer-stack.jpg
---

# 质子交换膜 (PEM)
**灵活性之王**

<v-clicks>

- **核心**: 固态聚合物电解质 (Nafion 膜)，工作温度 50-80°C。
- **性能指标**:
  - **电流密度**: 2-3 A/cm² (是 ALK 的 4-5 倍)。
  - **动态响应**: < 1秒 (0-100% 负载)，完美适配风光波动 [2]。
  - **系统寿命**: > 50,000 小时。
- **优势**: 结构紧凑，占地面积小，适合空间受限场景。
</v-clicks>

::right::

<div class="ml-4 mt-10">
  <img 
    v-motion
    :initial="{ opacity: 0, x: 50 }"
    :enter="{ opacity: 1, x: 0 }"
    src="https://telegraph.ttwwjj.ddns-ip.net/file/AgACAgUAAyEGAAShY8_eAAOZaSKru18kcVe7Ugjb1lCJ5tx2AAHjAAK2C2sb-AwZVTScd0PSrK8zAQADAgADeQADNgQ.png" 
    class="rounded-lg bg-white p-2"
  />
  <div class="text-center text-xs opacity-50 mt-2">PEM 实验装置示意图</div>
</div>

---
topic: pem
transition: fade-out
---

# PEM 的“贵族”烦恼

**铱 (Iridium) 的稀缺性**

<div class="flex gap-8 mt-8 items-center">
  <div class="w-1/2">
    <v-clicks>
      <div class="mb-4">
        <h3 class="font-bold text-red-400">资源瓶颈</h3>
        <p>铱是铂族金属副产物，年产量仅 ~7-9 吨。</p>
      </div>
      <div class="mb-4">
        <h3 class="font-bold text-yellow-400">成本占比</h3>
        <p>膜电极 (MEA) 占电解槽成本的 40% 以上。</p>
      </div>
      <div class="mb-4">
        <h3 class="font-bold text-green-400">解决方案</h3>
        <p>低铱/无铱催化剂研发 (目标: < 0.1 mg/cm²)。</p>
      </div>
    </v-clicks>
  </div>
  <div class="w-1/2">
    <div class="bg-gray-800 p-6 rounded-xl text-center">
      <div class="text-5xl font-mono mb-2">$1,200</div>
      <div class="text-sm opacity-60">PEM 系统当前 CAPEX (/kW)</div>
      <div class="h-px bg-gray-600 my-4"></div>
      <div class="text-5xl font-mono mb-2 text-green-400">$500</div>
      <div class="text-sm opacity-60">2030 目标 CAPEX (/kW)</div>
    </div>
  </div>
</div>




---
layout: image-right
image: https://www.researchgate.net/publication/375489108/figure/fig1/AS:11431281204076525@1699575640514/Schematic-of-anion-exchange-membrane-AEM-water-electrolyzer-membrane-electrode.jpg
topic: aem
transition: slide-left
---

# AEM: 完美的折中方案？

**结合 ALK 的低成本与 PEM 的高性能**

<v-clicks>

- **核心愿景**: 使用非贵金属催化剂 (Ni, Fe) 实现 PEM 级的电流密度 [3]。
- **技术难点**: 
  - 阴离子膜 (AEM) 的化学稳定性差。
  - 离子电导率低于质子膜。
- **最新突破**:
  - *Nature Energy (2023)*: 开发了新型聚合物骨架，在 60°C 下实现 **>1000小时** 稳定运行 [3][16]。
  - **商业化进程**: Enapter 等公司已推出 MW 级 AEM 模块，目标 LCOH < $2/kg [18]。

</v-clicks>

---
layout: two-cols
topic: seawater
transition: fade-out
background: https://assets.newatlas.com/dims4/default/13aba13/2147483647/strip/true/crop/1425x748+0+160/resize/1200x630!/quality/90/?url=https%3A%2F%2Fnewatlas-brightspot.s3.amazonaws.com%2F2a%2Fab%2F7631d2aa427b8c10bc183ff1c2cd%2Fscreenshot-2022-12-16-at-1.21.02%20pm.png&na.image_optimisation=0
---

# 海水直接电解

**向海洋要氢：解决淡水依赖**

<v-clicks>

- **背景**: 传统电解消耗大量高纯水 (9kg 水 / 1kg 氢)，海水淡化增加成本与复杂性。
- **挑战**: 海水中复杂的离子成分 (Cl⁻, Mg²⁺, Ca²⁺) 导致阳极腐蚀与结垢 [4]。
- **策略**:
  - **物理阻隔**: 利用疏水膜只允许水蒸气通过 (膜蒸馏耦合)。
  - **化学阻隔**: 在电极表面构建抗腐蚀层 (如 NiFe-LDH) [10]。

</v-clicks>

::right::

<div class="ml-4 mt-8">
  <img 
    src="https://www.science.org/do/10.1126/science.adh8151/abs/_20230317_NID_seawater.jpg" 
    class="rounded-lg shadow-lg border border-white/20"
  />
  <div class="text-center text-xs opacity-60 mt-2">
    海水直接电解装置示意图 [4]
  </div>
</div>

---
layout: center
topic: seawater
transition: view-transition
---

# 突破性机制：相变迁移

*Nature (2022) / Joule (2022)*

<div class="flex justify-center my-4">
  <img 
    src="https://en.szu.edu.cn/__local/B/A5/85/7CAD345EA2B4099CACFB28A300C_FAE36121_2AA24.png?e=.png" 
    class="h-52 rounded-lg shadow-2xl border border-white/10"
  />
</div>

<div class="flex justify-center mb-4">
  <div class="grid grid-cols-2 gap-4 w-3/4">
      <div class="bg-white/5 p-3 rounded-xl border border-white/10">
        <h3 class="text-base font-bold text-blue-400 mb-1">原理</h3>
        <p class="text-xs opacity-90">利用水蒸气分压差，海水自然蒸发穿过疏水膜，凝结为纯水后电解。</p>
      </div>
      <div class="bg-white/5 p-3 rounded-xl border border-white/10">
        <h3 class="text-base font-bold text-green-400 mb-1">优势</h3>
        <p class="text-xs opacity-90">彻底隔绝杂质离子，实现 **>3000小时** 稳定运行，无需额外淡化能耗 [4]。</p>
      </div>
  </div>
</div>

<div class="text-center text-sm opacity-60 mt-4">
  这一机制使得“海上风电+海水制氢”成为现实，构建深远海能源岛 [5]。
</div>

---
layout: image-left
image: https://www.offshorewind.biz/wp-content/uploads/sites/2/2023/06/Lhyfe_Sealhyfe-offshore-hydrogen-production-platform-and-Floatgen-floating-wind-turbine.jpg
topic: offshore
transition: slide-left
---

# 离岸制氢 (Offshore Hydrogen)

**深远海能源岛**

<v-clicks>

- **资源优势**: 远海风速更高 (>10 m/s) 且更稳定，不占用土地资源 [5]。
- **输送经济性**: 距离 >100km 时，氢气管道输送成本低于高压直流输电 (HVDC)。
- **示范项目**: 
  - **Lhyfe Sealhyfe**: 全球首个海上制氢平台，验证了 PEM 在风浪下的稳定性。
  - **PosHYdon**: 北海海上油气平台改造制氢。
- **挑战**: 盐雾腐蚀、高昂的运维成本 (O&M 约为陆上的 3-5 倍) [5]。

</v-clicks>

---
layout: two-cols
topic: pec
transition: fade-out
background: https://images.unsplash.com/photo-1454779132693-e5cd0a216ed3?q=80&w=2070&auto=format&fit=crop
class: text-left
---

# 前沿探索：光电化学 (PEC)

**人工光合作用：一步法制氢**

<v-clicks>

- **原理**: 半导体光电极直接吸收太阳光分解水，无需外接电源。
- **关键指标**: 太阳能转化氢能效率 (STH)。
  - 当前水平: ~10% (实验室) [14]。
  - 商业化门槛: >15-20%。
- **材料体系**: 
  - 金属氧化物 ($Fe_2O_3$, $BiVO_4$): 稳定但效率低。
  - III-V 族半导体 / 钙钛矿: 效率高但易腐蚀/昂贵。

</v-clicks>

::right::

<div class="ml-4 mt-10">
  <img 
    src="https://ooo.0x0.ooo/2023/03/31/21lRS.png" 
    class="rounded-lg shadow-2xl bg-black/40 p-2"
  />
  <div class="text-center text-xs opacity-60 mt-2">
    典型 PEC 器件结构示意图
  </div>
</div>

---
layout: center
topic: future
transition: slide-up
background: https://images.unsplash.com/photo-1466611653911-95081537e5b7?q=80&w=2070&auto=format&fit=crop
class: text-center
---

# 全球格局与未来展望

<div class="grid grid-cols-3 gap-6 mt-8 text-left">
  <div class="bg-black/50 p-4 rounded-lg backdrop-blur-sm">
    <h3 class="text-xl font-bold text-blue-400 mb-2">规模化</h3>
    <p class="text-sm opacity-90">2025年全球产能突破 1 Mt/yr，中国占据主导地位 (60%+) [2][11]。</p>
  </div>
  <div class="bg-black/50 p-4 rounded-lg backdrop-blur-sm">
    <h3 class="text-xl font-bold text-green-400 mb-2">成本下降</h3>
    <p class="text-sm opacity-90">随着电解槽制造自动化，预计 2030 年绿氢成本降至 $2-3/kg [1][6]。</p>
  </div>
  <div class="bg-black/50 p-4 rounded-lg backdrop-blur-sm">
    <h3 class="text-xl font-bold text-purple-400 mb-2">应用拓展</h3>
    <p class="text-sm opacity-90">从化工脱碳向钢铁冶炼、重卡运输及航运燃料 (氨/甲醇) 延伸 [15]。</p>
  </div>
</div>

<div class="mt-12 text-sm opacity-70">
  "氢能不是唯一的答案，但它是净零排放拼图中不可或缺的一块。" — IEA Global Hydrogen Review 2025
</div>

---
layout: center
transition: fade-out
class: text-left
---

# 参考文献

<div class="text-xs opacity-70 leading-relaxed columns-2 gap-8">

1. **IRENA**. (2024). *Global Hydrogen Trade Outlook*.
2. **IEA**. (2025). *Global Hydrogen Review 2025*.
3. **Nature Energy**. (2023). *Stable anion exchange membranes*.
4. **Joule**. (2022). *Direct seawater electrolysis*.
5. **NREL**. (2024). *Offshore Wind for Hydrogen*.
6. **Springer**. (2025). *Green hydrogen production and deployment*.
7. **Energies Media**. (2025). *Hydrogen Energy in 2025*.
8. **ScienceDirect**. (2025). *Advancements in green hydrogen production*.
9. **Newswise**. (2025). *Recent Progress of Green Hydrogen Production Technology*.
10. **PMC**. (2025). *Recent Advances in Green Hydrogen Production by Electrolyzing Water*.
11. **Yahoo Finance**. (2025). *2025 Green Hydrogen Market Technology Landscape*.
12. **StartUs Insights**. (2024). *Top 10 Hydrogen Trends in 2025*.
13. **Airswift**. (2025). *Top US green hydrogen projects for 2025*.
14. **ACS Catalysis**. (2024). *Transition metal-based catalysts*.
15. **IRENA**. (2025). *Green hydrogen for industrial decarbonisation (Central Asia & South Caucasus)*.
16. **Frontiers in Membrane Science and Technology**. (2025). *Grand challenges in anion exchange membrane energy applications*.
17. **WIREs Energy and Environment**. (2025). *Advancements in Electrode Development for Water Electrolysis*.
18. **Fuel Cells Works**. (2025). *GS E&C Enters Hydrogen Tech Market with EVOLOH AEM Electrolysis*.

</div>

<div class="absolute bottom-4 right-4 text-xs opacity-30">
  Powered by Slidev
  <br></br>
  源代码:https://github.com/twj0/slidev-demo
</div>
