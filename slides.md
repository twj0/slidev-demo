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
layout: center
transition: slide-left
class: text-left
background: https://www.nrel.gov/images/libraries/news/program/2024/20240715-offshore-wind-turbines-offer-path-for-clean-hydrogen-production-84771.jpg?sfvrsn=60d0f078_0
---

# 全球氢能现状（2025）

<v-clicks>

- **年度需求**：约 1 亿吨 H₂，其中**低排放氢**（绿氢 + 蓝氢）占比 < 1%，但 2024 年起保持约 **10%/年增长**。  
- **生产结构**：约 **75%** 来自化石燃料蒸汽甲烷重整 (SMR)，煤气化约 15%，工业副产氢 < 5%。  
- **减排缺口**：IEA 预测，为实现净零情景，2030 年需要 **3,700 万吨低排放氢**，而当前项目仅覆盖目标的约三分之一。  
- **视觉参考**：SMR+CCUS 流程图、电解水装置结构示意和海水电解电极设计等图像，有助于直观理解不同制氢路径在流程与材料上的差异。  
- **区域差异**：欧盟、日本更依赖进口绿氢与合成燃料，中国、中东等地区则更多利用本地可再生能源与化石资源组合（IEA, IRENA 2025）。  

</v-clicks>

<div class="mt-6 text-xs opacity-60">
  数据来源：IEA <i>Global Hydrogen Review 2025</i>，IRENA 氢能报告等公开资料
</div>
 
---
layout: center
transition: slide-left
class: text-left
---

# 化石制氢路径对比

| 路径 | 主要反应 | 典型效率 | CO₂ 排放 (kg/kg H₂) | 成本 ($/kg, 2025) | 全球占比 |
|------|----------|----------|---------------------|-------------------|----------|
| SMR 灰氢 | $CH_4 + H_2O \\rightleftharpoons CO + 3H_2$ | 70–85% | **9–12** | 1.5–3 | ~75% |
| SMR+CCUS 蓝氢 | 同上 + CO₂ 捕集 | 70–80% | **< 2** | 2–4 | ~20% |
| 煤气化 | $C + H_2O \\rightarrow CO + H_2$ | 60–70% | **15–20** | 1–2 | ~15% |
| 工业副产氢 | 氯碱、焦炉煤气等 | 80%+ | 视工艺而定 | 0.5–2 | <5% |

<div class="mt-4 text-xs opacity-60">
  数据综合自 IEA <i>Global Hydrogen Review 2025</i> 及相关综述，仅供定量比较参考。传统化石制氢占当前供应绝大部分，后续报告将重点聚焦电解水及其前沿技术路线。
</div>

---
layout: image-right
image: https://images.unsplash.com/photo-1468787737698-f5c03f0570dd?q=80&w=2070&auto=format&fit=crop
transition: slide-left
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
layout: two-cols
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
transition: slide-left
---

# ALK 的规模化之路

**中国供应链的统治力**

<v-clicks>

- **单槽规模**: 从 5 MW 迈向 **10-20 MW**。
- **产氢量**: 单体可达 **2000-4000 Nm³/h**。
- **CAPEX**: 中国厂商报价低至 **$300/kW** (欧美约为 $800/kW)。
- **技术迭代**: 
  - 零极距设计 (Zero-gap)
  - 高性能隔膜 (Zirfon) 降低内阻

</v-clicks>

<br>

<div v-click class="bg-orange-500/10 p-3 rounded text-sm">
  ⚠️ <b>挑战:</b> 动态响应较慢，冷启动时间长，难以完美跟随风光剧烈波动。
</div>

---
layout: two-cols
transition: slide-left
background: https://www.researchgate.net/publication/339946556/figure/fig1/AS:869574543147008@1584334135629/Experimental-setup-the-high-pressure-characterization-of-PEM-electrolyzer-stack.jpg
---

# 质子交换膜 (PEM)
**灵活性之王**

<v-clicks>

- **核心**: 固态聚合物电解质 (Nafion 膜)。
- **结构**: 紧凑的“零间隙”结构，高压运行 (30-70 bar)。
- **优势**:
  - **秒级响应**: 0-100% 负载切换仅需毫秒。
  - **高电流密度**: 可达 2-3 A/cm²。
  - **占地小**: 适合空间受限场景。

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
layout: center
transition: view-transition
---

# 典型案例研究

<div class="grid grid-cols-2 gap-12 mt-8 w-full max-w-5xl">

<div class="relative group cursor-pointer">
  <div class="absolute inset-0 bg-blue-500/20 blur-xl group-hover:bg-blue-500/30 transition"></div>
  <div class="relative bg-black/40 p-6 rounded-xl border border-blue-500/50 h-full">
    <h3 class="text-xl font-bold mb-2">🇯🇵 Fukushima FH2R</h3>
    <div class="text-blue-400 text-sm mb-4">10 MW ALK 系统</div>
    <ul class="text-sm list-disc pl-4 space-y-2 opacity-80">
      <li>全球最大级可再生能源制氢项目</li>
      <li>利用 AI 预测模型优化运行</li>
      <li>验证了 ALK 在波动电源下的适应性</li>
    </ul>
  </div>
</div>

<div class="relative group cursor-pointer">
  <div class="absolute inset-0 bg-green-500/20 blur-xl group-hover:bg-green-500/30 transition"></div>
  <div class="relative bg-black/40 p-6 rounded-xl border border-green-500/50 h-full">
    <h3 class="text-xl font-bold mb-2">🇪🇺 Shell Refhyne</h3>
    <div class="text-green-400 text-sm mb-4">10 MW PEM 系统</div>
    <ul class="text-sm list-disc pl-4 space-y-2 opacity-80">
      <li>位于德国莱茵兰炼油厂</li>
      <li>提供电网频率响应服务</li>
      <li>计划扩建至 100 MW</li>
    </ul>
  </div>
</div>

</div>

---
transition: slide-up
---

# 技术参数深度对比

| 参数 | 碱性电解 (ALK) | 质子交换膜 (PEM) | 阴离子交换膜 (AEM) |
| :--- | :---: | :---: | :---: |
| **电解质** | 液体 KOH | 固态聚合物 | 固态聚合物 |
| **工作温度** | 60-80°C | 50-80°C | 50-60°C |
| **电流密度** | 0.4-0.6 A/cm² | **2.0-3.0 A/cm²** | 0.5-2.0 A/cm² |
| **负载范围** | 15-100% | **0-160%** | 5-100% |
| **冷启动** | ~50 分钟 | **< 5 分钟** | ~10 分钟 |
| **关键材料** | 镍, 不锈钢 | 铂, 铱, 钛 | 镍, 铁, 钢 |
| **系统寿命** | > 80,000 h | > 50,000 h | < 5,000 h (目前) |
| **CAPEX** | **$** | **$$$** | **$** (潜力) |

<div v-click class="mt-6 text-center text-sm opacity-70">
  数据来源: IEA Global Hydrogen Review & IRENA Reports
</div>

---
layout: image-right
image: https://www.researchgate.net/publication/375489108/figure/fig1/AS:11431281204076525@1699575640514/Schematic-of-anion-exchange-membrane-AEM-water-electrolyzer-membrane-electrode.jpg
transition: slide-left
---

# AEM: 完美的折中方案？

**结合 ALK 的低成本与 PEM 的高性能**

<v-clicks>

- **核心愿景**: 使用非贵金属催化剂 (Ni, Fe) 实现 PEM 级的电流密度。
- **技术难点**: 
  - 阴离子膜 (AEM) 的化学稳定性差。
  - 离子电导率低于质子膜。
- **最新突破**:
  - *Nature Energy (2023)*: 开发了新型聚合物骨架，在 60°C 下实现 **>1000小时** 稳定运行。
  - 商业化前夜: Enapter 等公司已推出 kW 级 AEM 模块。

</v-clicks>

---
layout: two-cols
transition: fade-out
background: https://assets.newatlas.com/dims4/default/13aba13/2147483647/strip/true/crop/1425x748+0+160/resize/1200x630!/quality/90/?url=https%3A%2F%2Fnewatlas-brightspot.s3.amazonaws.com%2F2a%2Fab%2F7631d2aa427b8c10bc183ff1c2cd%2Fscreenshot-2022-12-16-at-1.21.02%20pm.png&na.image_optimisation=0
---

# 海水直接电解

**向海洋要氢**

<v-clicks>

- **背景**: 传统电解消耗大量高纯水 (9kg 水 / 1kg 氢)。
- **痛点**: 海水中复杂的离子成分 (Cl⁻, Mg²⁺, Ca²⁺)。
- **氯腐蚀**: 阳极析氯反应 (CER) 与析氧反应 (OER) 竞争，腐蚀电极。

</v-clicks>

::right::

<div class="ml-4 mt-8">
  <h3 class="text-lg font-bold mb-2">主要策略</h3>
  <ul class="space-y-4">
    <li v-click class="bg-white/5 p-3 rounded">
      <span class="text-blue-400 font-bold">物理阻隔</span>
      <p class="text-sm opacity-80">利用疏水膜只允许水蒸气通过 (膜蒸馏耦合)。</p>
    </li>
    <li v-click class="bg-white/5 p-3 rounded">
      <span class="text-green-400 font-bold">化学阻隔</span>
      <p class="text-sm opacity-80">在电极表面构建抗腐蚀层 (如 NiFe-LDH)。</p>
    </li>
  </ul>
</div>

---
layout: center
transition: view-transition
---

# 突破性机制：相变迁移

*Nature (2022/2024) - 谢和平院士团队 / 斯坦福大学*

<div class="flex justify-center my-6">
  <img 
    src="https://en.szu.edu.cn/__local/B/A5/85/7CAD345EA2B4099CACFB28A300C_FAE36121_2AA24.png?e=.png" 
    class="h-60 rounded-lg shadow-2xl"
  />
</div>

<v-clicks>

1. **原理**: 利用水蒸气分压差。
2. **过程**: 海水 -> 蒸发 -> 穿过疏水膜 -> 凝结为纯水 -> 电解。
3. **效果**: 彻底隔绝了杂质离子，实现了 **>3000小时** 的稳定运行。
4. **意义**: 使得“海上风电+海水制氢”成为现实，无需额外的海水淡化设备。

</v-clicks>

---
layout: image-left
image: https://www.offshorewind.biz/wp-content/uploads/sites/2/2023/06/Lhyfe_Sealhyfe-offshore-hydrogen-production-platform-and-Floatgen-floating-wind-turbine.jpg
transition: slide-left
---

# 离岸制氢 (Offshore Hydrogen)

**深远海能源岛**

<v-clicks>

- **资源**: 远海风速更高、更稳定 (>10 m/s)。
- **输送**: 
  - 电力传输 (HVDC): 昂贵。
  - **氢气管道**: 距离 >100km 时成本更低。
- **挑战**:
  - 极端环境 (盐雾、风浪)。
  - 平台稳定性 (漂浮式风机耦合)。
  - 运维成本 (O&M) 是陆上的 3-5 倍。

</v-clicks>

<div v-click class="mt-4 text-xs opacity-60">
  图: Lhyfe Sealhyfe 离岸制氢平台原型
</div>

---
transition: fade-out
---

# 前沿探索：光电化学 (PEC)

**人工光合作用**

<div class="grid grid-cols-2 gap-8 mt-8">

<div>
  <h3 class="text-xl font-bold text-yellow-400 mb-4">一步法制氢</h3>
  <p class="mb-4">直接利用太阳光驱动半导体催化剂分解水，无需外接电源。</p>
  
  <div v-click class="bg-white/5 p-4 rounded-lg">
    <div class="font-bold">关键指标: STH (Solar-to-Hydrogen)</div>
    <div class="flex justify-between mt-2 text-sm">
      <span>当前水平:</span>
      <span class="text-yellow-400">~10%</span>
    </div>
    <div class="flex justify-between mt-1 text-sm">
      <span>商业化门槛:</span>
      <span class="text-green-400">>15-20%</span>
    </div>
  </div>
</div>

<div class="flex flex-col justify-center">
  <div class="relative rounded-xl overflow-hidden bg-slate-900/60">
    <img 
      src="https://ooo.0x0.ooo/2023/03/31/21lRS.png" 
      class="absolute inset-0 w-full h-full object-cover opacity-60"
    />
    <div class="relative p-4 backdrop-blur-sm bg-gradient-to-r from-slate-900/80 to-slate-800/40">
      <h4 class="font-bold">典型 PEC 器件结构</h4>
      <p class="text-sm mt-2 opacity-90">
        光阳极/光阴极吸收太阳光产生光生载流子，在电解质中完成水分解反应；常见体系包括金属氧化物、III-V 半导体与钙钛矿叠层等。
      </p>
      <p class="text-sm mt-2 opacity-80">
        当前研究重点在于提高光吸收与催化活性，同时兼顾长期稳定性与低成本封装，使 PEC 有望在分布式“光照即产氢”场景中落地。
      </p>
      <p class="text-xs mt-2 opacity-70">
        图：典型光电化学水分解装置示意。
      </p>
    </div>
  </div>
</div>

</div>

---
layout: cover
background: https://images.unsplash.com/photo-1466611653911-95081537e5b7?q=80&w=2070&auto=format&fit=crop
class: text-center
transition: slide-up
---

# 先进制氢工艺总览
## Advanced Hydrogen Production

<v-clicks>

 - **高端电解水体系 (ALK / PEM / AEM / SOEC)**：从常温到高温电解，目标是把能耗压到 30–55 kWh/kg H₂，并在 MW–GW 级保持高电流密度与长寿命。  
 - **海水直接电解**：利用疏水膜和相变迁移等结构，在电极侧形成“原位淡水层”，抑制 Cl⁻ 腐蚀与结垢，实验室与中试装置已实现 >1000 h 稳定运行。  
 - **光电化学 (PEC) 与光催化**：半导体吸光驱动水分解，当前 STH 约 5–12%，实验室装置接近 10%，商业化通常认为需 >15–20%。  

</v-clicks>

<div class="mt-6 text-xs opacity-60">
  数据来源：IEA、IRENA 相关氢能技术报告及多篇电解水/PEC/生物质制氢综述。
</div>

---
layout: two-cols
transition: slide-left
class: text-left
---

# 世界领军制氢项目与企业

<v-clicks>

 - **日本 Fukushima FH2R (ALK)**：10 MW 级碱性电解槽 + 20 MW 光伏与储能，通过 AI 调度验证 ALK 在波动电源下的长期稳定运行。  
 - **德国 Shell Refhyne (PEM)**：10 MW PEM 为莱茵兰炼油厂供氢并参与电网调频，规划扩展至 100 MW 级。  
 - **Enapter / EVOLOH + GS E&C (AEM)**：模块化 AEM 从 kW 扩展到 MW，目标是用非贵金属催化剂实现高电流密度和低 CAPEX。  
 - **Lhyfe Sealhyfe 离岸制氢平台**：在漂浮式风机旁布置 1 MW PEM 模块，为未来更大规模“海上制氢岛”积累工程经验。  

</v-clicks>

::right::

<div class="mt-4">
  <img 
    src="https://images.unsplash.com/photo-1487875961445-47a00398c267?q=80&w=1600&auto=format&fit=crop" 
    class="rounded-lg shadow-lg border border-white/10"
  />
  <div class="text-center text-xs opacity-60 mt-2">
    绿氢工厂与工业电解槽总装示意（Unsplash 自由图片）
  </div>
</div>

<div class="mt-6 text-xs opacity-60">
  参考：项目公开资料、IEA 与行业报告；EVOLOH + GS E&C 合作新闻，Lhyfe Sealhyfe 官方发布等。
</div>

---
layout: two-cols
transition: fade-out
background: https://images.unsplash.com/photo-1454779132693-e5cd0a216ed3?q=80&w=2070&auto=format&fit=crop
class: text-left
---

# 下一代制氢方向与研发热点

<v-clicks>

 - **低铱/无铱 PEM 电解槽**：通过纳米结构与合金设计大幅降低阳极铱用量，目标是在 2–3 A/cm² 下把系统 CAPEX 压到 **300–500 $/kW**。  
 - **高电流密度 AEM 与非贵金属催化剂**：Ni/Fe 等非贵金属体系在 AEM 中已实现 **1–2 A/cm²、>1000 h**，下一步是提升膜稳定性并实现卷对卷制膜与自动化堆栈装配。  
 - **大规模海水电解**：基于相变迁移和多层防护结构，把实验室方案放大到 MW 级，与海上风电、漂浮光伏和海水淡化耦合，构建“海上制氢 + 管道回输”一体化系统。  
 - **光电化学与光催化新体系**：发展稳定的钙钛矿/Si 叠层 PEC 和高效率光催化粉体，并用机器学习 + 高通量计算加速材料筛选，缩短从发现到工程应用的周期。  

</v-clicks>

  <div class="mt-6 text-xs opacity-60">
    参考：近年关于 PEM/AEM/海水电解与 PEC 的综述与前沿论文，以及主要设备供应商的技术路线图。
  </div>
 
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
  Powered by Slidev & Antigravity
</div>
