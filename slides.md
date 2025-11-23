---
theme: seriph
background: https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=2072&auto=format&fit=crop
title: 氢气制取技术：产业与学术前沿
info: |
  ## 氢气制取技术：产业与学术前沿
  面向可再生能源概论课程
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: view-transition
css: unocss
mdc: true
---

# 氢气制取技术：产业与学术前沿

<div class="text-2xl opacity-80 mt-4">
面向可再生能源概论课程
</div>

<div class="abs-br m-6 flex gap-2">
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
transition: fade-out
---

# 氢的色彩光谱

<div class="grid grid-cols-3 gap-6 mt-10">

<div v-click class="text-center p-4 bg-gray-100 rounded-xl dark:bg-gray-800">
  <div class="text-4xl mb-2">🌑</div>
  <h3 class="text-gray-600 font-bold">灰氢 (Grey)</h3>
  <p class="text-sm mt-2 opacity-70">化石燃料重整</p>
  <p class="text-xs mt-1 text-red-500">高碳排放</p>
</div>

<div v-click class="text-center p-4 bg-blue-50 rounded-xl dark:bg-blue-900/30">
  <div class="text-4xl mb-2">🔵</div>
  <h3 class="text-blue-600 font-bold">蓝氢 (Blue)</h3>
  <p class="text-sm mt-2 opacity-70">化石燃料 + CCUS</p>
  <p class="text-xs mt-1 text-yellow-500">低碳排放</p>
</div>

<div v-click class="text-center p-4 bg-green-50 rounded-xl dark:bg-green-900/30 border-2 border-green-500">
  <div class="text-4xl mb-2">🟢</div>
  <h3 class="text-green-600 font-bold">绿氢 (Green)</h3>
  <p class="text-sm mt-2 opacity-70">可再生能源电解水</p>
  <p class="text-xs mt-1 text-green-500">零碳排放</p>
</div>

</div>

<div v-click class="mt-8 text-center text-lg font-serif italic">
  "绿氢是实现 2050 净零排放的终极方案。"
</div>

---
layout: center
class: text-center
transition: view-transition
---

# 技术全景图
## The Technology Landscape

<div class="grid grid-cols-2 gap-8 mt-8 text-left max-w-4xl mx-auto">
  <div v-click class="border p-4 rounded hover:bg-white/5 transition">
    <h3 class="text-xl font-bold text-blue-400">ALK</h3>
    <p class="opacity-70">碱性电解水</p>
    <div class="text-sm mt-2">成熟度: High | 成本: Low</div>
  </div>
  <div v-click class="border p-4 rounded hover:bg-white/5 transition">
    <h3 class="text-xl font-bold text-green-400">PEM</h3>
    <p class="opacity-70">质子交换膜</p>
    <div class="text-sm mt-2">成熟度: Medium | 响应: Fast</div>
  </div>
  <div v-click class="border p-4 rounded hover:bg-white/5 transition">
    <h3 class="text-xl font-bold text-purple-400">AEM</h3>
    <p class="opacity-70">阴离子交换膜</p>
    <div class="text-sm mt-2">成熟度: Low | 潜力: High</div>
  </div>
  <div v-click class="border p-4 rounded hover:bg-white/5 transition">
    <h3 class="text-xl font-bold text-cyan-400">Seawater</h3>
    <p class="opacity-70">海水直接电解</p>
    <div class="text-sm mt-2">成熟度: R&D | 资源: Unlimited</div>
  </div>
</div>

---
layout: cover
background: https://images.unsplash.com/photo-1504917595217-d4dc5ebe6122?q=80&w=2070&auto=format&fit=crop
class: text-center
transition: slide-up
---

# 产业前沿
## Industrial Frontiers
成熟度与规模化部署

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
layout: cover
background: https://images.unsplash.com/photo-1532094349884-543bc11b234d?q=80&w=2070&auto=format&fit=crop
class: text-center
transition: slide-up
---

# 学术前沿
## Academic Innovations
新材料、新工艺与海洋应用

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
  <div v-click class="p-4 border-l-2 border-purple-500 bg-purple-500/10">
    <h4 class="font-bold">AI 加速材料发现</h4>
    <p class="text-sm mt-2 opacity-80">
      利用机器学习 (ML) 和密度泛函理论 (DFT) 筛选数万种钙钛矿材料，寻找最佳带隙匹配。
    </p>
  </div>
</div>

</div>

---
layout: cover
background: https://images.unsplash.com/photo-1466611653911-95081537e5b7?q=80&w=2070&auto=format&fit=crop
class: text-center
transition: slide-up
---

# 未来展望
## Future Outlook
路线图与结语

---
transition: slide-left
---

# 2025-2050 技术路线图

<div class="relative mt-10 mx-10">
  <!-- Line -->
  <div class="absolute left-4 top-0 bottom-0 w-1 bg-gray-700"></div>

  <!-- Nodes -->
  <div v-click class="relative pl-12 mb-8">
    <div class="absolute left-2 top-2 w-5 h-5 bg-green-500 rounded-full -translate-x-1/2 border-4 border-gray-900"></div>
    <h3 class="text-xl font-bold text-green-400">2025: 规模化起步</h3>
    <p class="opacity-70">ALK 单槽 10MW+; 示范项目遍地开花; 成本 ~$4-5/kg。</p>
  </div>

  <div v-click class="relative pl-12 mb-8">
    <div class="absolute left-2 top-2 w-5 h-5 bg-blue-500 rounded-full -translate-x-1/2 border-4 border-gray-900"></div>
    <h3 class="text-xl font-bold text-blue-400">2030: 成本拐点</h3>
    <p class="opacity-70">绿氢成本降至 $2-3/kg (与蓝氢持平); AEM 开始商业化; 离岸制氢试点。</p>
  </div>

  <div v-click class="relative pl-12">
    <div class="absolute left-2 top-2 w-5 h-5 bg-purple-500 rounded-full -translate-x-1/2 border-4 border-gray-900"></div>
    <h3 class="text-xl font-bold text-purple-400">2050: 深度脱碳</h3>
    <p class="opacity-70">绿氢成为主力能源; 海水直接电解普及; 全球氢能贸易网络成熟。</p>
  </div>
</div>

---
layout: center
class: text-center
transition: fade-out
---

# 结语

<div class="text-3xl font-serif italic mb-8">
"氢能不是万能药，但没有氢能，净零排放将是空谈。"
</div>

<v-clicks>

- **产业界**: 致力于降本增效 (Scale-up)。
- **学术界**: 致力于突破材料极限 (Innovation)。
- **政策**: 需要持续的碳价机制支持。

</v-clicks>

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

</div>

<div class="absolute bottom-4 right-4 text-xs opacity-30">
  Powered by Slidev & Antigravity
</div>
