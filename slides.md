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

<!-- Slide 1: Title -->
<div class="absolute inset-0 bg-gradient-to-br from-black/90 via-blue-900/50 to-teal-900/50 z-0 animate-gradient"></div>

<div class="relative z-10 h-full flex flex-col justify-center items-center text-white perspective-1000">
  <div v-motion
       :initial="{ rotateX: 20, scale: 0.8, opacity: 0, filter: 'blur(10px)' }"
       :enter="{ rotateX: 0, scale: 1, opacity: 1, filter: 'blur(0px)', transition: { duration: 1200, type: 'spring' } }"
       class="mb-6 transform-3d">
    <div class="text-8xl font-black bg-clip-text text-transparent bg-gradient-to-r from-teal-400 via-blue-500 to-purple-500 drop-shadow-[0_0_35px_rgba(45,212,191,0.8)]">
      绿氢制取
    </div>
    <div class="text-4xl font-light tracking-[0.8em] mt-8 text-gray-300 uppercase border-t border-b border-white/20 py-4">
      Green Hydrogen
    </div>
  </div>
  
  <div class="abs-br m-8 flex items-center gap-4 opacity-60">
    <div class="text-right">
      <div class="text-xs font-mono text-teal-400">2025 EDITION</div>
      <div class="text-xs font-mono text-white">Advanced Energy Report</div>
    </div>
    <div class="w-12 h-12 rounded-full border-2 border-teal-400/50 flex items-center justify-center animate-spin-slow">
      <div class="i-carbon-hydrogen text-2xl text-teal-400"></div>
    </div>
  </div>
</div>

<style>
@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
.animate-gradient {
  background-size: 200% 200%;
  animation: gradient 15s ease infinite;
}
.animate-spin-slow {
  animation: spin 10s linear infinite;
}
@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
</style>

---
layout: default
---

<!-- Slide 2: The Hook -->
# 核心命题：制取成本
### The Cost Bottleneck

<div class="flex justify-center items-center h-full">
  <div class="text-center space-y-12 relative">
    <!-- Background Glow -->
    <div class="absolute inset-0 bg-blue-500/10 blur-3xl rounded-full -z-10"></div>

    <div class="text-5xl font-bold text-gray-200 leading-tight" v-motion-slide-visible-bottom>
      氢能经济的<span class="text-teal-400 text-7xl mx-2 inline-block transform hover:scale-110 transition">基石</span>
      <br>也是目前的<span class="text-red-400 text-7xl mx-2 inline-block transform hover:scale-110 transition">短板</span>
    </div>
    
    <div class="grid grid-cols-2 gap-8 max-w-4xl mx-auto mt-8">
      <div class="bg-gray-800/50 p-6 rounded-xl border border-gray-700 backdrop-blur-sm" v-motion-slide-visible-bottom :delay="200">
        <div class="text-4xl font-bold text-teal-400 mb-2">60-75%</div>
        <div class="text-sm text-gray-400">Current Efficiency (LHV)</div>
      </div>
      <div class="bg-gray-800/50 p-6 rounded-xl border border-gray-700 backdrop-blur-sm" v-motion-slide-visible-bottom :delay="300">
        <div class="text-4xl font-bold text-red-400 mb-2">$300-1200</div>
        <div class="text-sm text-gray-400">CAPEX per kW (2025)</div>
      </div>
    </div>
  </div>
</div>

---
layout: default
---

<!-- Slide 3: The Split -->
# 两大前沿阵地
### Two Frontiers

<div class="grid grid-cols-2 gap-12 mt-12 px-8 h-[350px]">
  <!-- Industrial Card -->
  <div class="group relative perspective-1000 cursor-pointer" v-click>
    <div class="absolute inset-0 bg-teal-500/20 rounded-2xl blur-xl group-hover:blur-3xl transition duration-500 opacity-0 group-hover:opacity-100"></div>
    <div class="relative h-full bg-gradient-to-br from-gray-900 to-gray-800 border border-teal-500/30 rounded-2xl p-8 flex flex-col justify-between hover:scale-[1.02] transition duration-500 shadow-2xl">
      <div>
        <div class="text-6xl mb-6 bg-gray-800 w-20 h-20 rounded-full flex items-center justify-center border border-teal-500/50">🏭</div>
        <h3 class="text-4xl font-bold text-teal-400">产业前沿</h3>
        <p class="text-xl text-gray-400 mt-2">Industrial Scale-up</p>
      </div>
      <div class="space-y-2">
        <div class="flex items-center text-sm text-teal-200"><div class="i-carbon-checkmark-filled mr-2"></div> 10MW+ Systems</div>
        <div class="flex items-center text-sm text-teal-200"><div class="i-carbon-checkmark-filled mr-2"></div> Cost Reduction</div>
      </div>
    </div>
  </div>

  <!-- Academic Card -->
  <div class="group relative perspective-1000 cursor-pointer" v-click>
    <div class="absolute inset-0 bg-purple-500/20 rounded-2xl blur-xl group-hover:blur-3xl transition duration-500 opacity-0 group-hover:opacity-100"></div>
    <div class="relative h-full bg-gradient-to-br from-gray-900 to-gray-800 border border-purple-500/30 rounded-2xl p-8 flex flex-col justify-between hover:scale-[1.02] transition duration-500 shadow-2xl">
      <div>
        <div class="text-6xl mb-6 bg-gray-800 w-20 h-20 rounded-full flex items-center justify-center border border-purple-500/50">🔬</div>
        <h3 class="text-4xl font-bold text-purple-400">学术前沿</h3>
        <p class="text-xl text-gray-400 mt-2">Academic Innovation</p>
      </div>
      <div class="space-y-2">
        <div class="flex items-center text-purple-200"><div class="i-carbon-flask mr-2"></div> New Materials (AEM)</div>
        <div class="flex items-center text-purple-200"><div class="i-carbon-waves mr-2"></div> Seawater Electrolysis</div>
      </div>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 4: ALK Visual Intro -->
<div class="w-full h-full bg-black relative overflow-hidden group">
  <img src="https://s7d1.scene7.com/is/image/CENODS/10121-cover-electrolyzer?$hero$&fmt=webp" 
       class="absolute inset-0 w-full h-full object-cover opacity-60 group-hover:scale-105 transition duration-[2000ms]"
       style="view-transition-name: alk-img" />
  
  <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent to-black/50"></div>

  <div class="absolute inset-0 flex flex-col items-center justify-center">
    <h1 class="text-[12rem] font-black text-transparent bg-clip-text bg-gradient-to-b from-white to-gray-500 tracking-tighter drop-shadow-2xl" 
        v-motion
        :initial="{ y: 100, opacity: 0 }"
        :enter="{ y: 0, opacity: 1, transition: { duration: 800 } }">
      ALK
    </h1>
    <div class="text-2xl text-teal-400 font-mono tracking-widest bg-black/50 px-4 py-1 rounded border border-teal-500/30 backdrop-blur-md">
      ALKALINE ELECTROLYSIS
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 5: ALK Scale-up -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden flex">
  <!-- Image moves to left half -->
  <div class="w-1/2 h-full relative overflow-hidden">
    <img src="https://s7d1.scene7.com/is/image/CENODS/10121-cover-electrolyzer?$hero$&fmt=webp" 
         class="absolute inset-0 w-full h-full object-cover opacity-60"
         style="view-transition-name: alk-img" />
    <div class="absolute inset-0 bg-gradient-to-r from-teal-900/20 to-gray-900"></div>
    
    <!-- Floating Stats -->
    <div class="absolute bottom-10 left-10 space-y-4">
       <div class="bg-black/60 backdrop-blur-md p-4 rounded-lg border-l-4 border-teal-500" v-motion-slide-visible-left>
         <div class="text-xs text-gray-400">Single Stack Output</div>
         <div class="text-2xl font-bold text-white">2000 Nm³/h</div>
       </div>
    </div>
  </div>

  <!-- Text appears on right -->
  <div class="w-1/2 h-full flex flex-col justify-center px-12 z-10 bg-gray-900">
    <h2 class="text-6xl font-bold text-teal-400 mb-8 leading-tight" v-motion-slide-visible-right>
      The 10 MW+<br>Era
    </h2>
    <div class="space-y-6">
      <p class="text-xl text-gray-300 leading-relaxed" v-motion-slide-visible-right :delay="100">
        碱性电解槽正在经历<b>巨型化</b>变革。单槽产氢量翻倍，大幅降低系统 BOP 成本。
      </p>
      <div class="grid grid-cols-2 gap-4" v-motion-slide-visible-right :delay="200">
        <div class="bg-gray-800 p-4 rounded-lg border border-gray-700">
          <div class="text-3xl font-bold text-white mb-1">20-30%</div>
          <div class="text-xs text-gray-400">BOP Cost Reduction</div>
        </div>
        <div class="bg-gray-800 p-4 rounded-lg border border-gray-700">
          <div class="text-3xl font-bold text-white mb-1">60-80°C</div>
          <div class="text-xs text-gray-400">Operating Temp</div>
        </div>
      </div>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 6: ALK Mechanism -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden p-8 flex items-center">
  <!-- Image shrinks to top-left corner -->
  <div class="absolute top-8 left-8 w-40 h-24 rounded-lg overflow-hidden border border-teal-500/30 z-20 opacity-50 grayscale hover:grayscale-0 transition">
    <img src="https://s7d1.scene7.com/is/image/CENODS/10121-cover-electrolyzer?$hero$&fmt=webp" 
         class="w-full h-full object-cover"
         style="view-transition-name: alk-img" />
  </div>

  <div class="w-full max-w-6xl mx-auto grid grid-cols-2 gap-12 items-center">
    <!-- Left: Schematic -->
    <div class="relative bg-white rounded-xl overflow-hidden shadow-2xl border-4 border-gray-800" v-motion-slide-visible-left>
      <img src="https://ars.els-cdn.com/content/image/1-s2.0-S2352484722020625-gr3.jpg" class="w-full object-contain p-4" />
      <div class="absolute bottom-0 inset-x-0 bg-black/70 p-2 text-center text-white text-xs">
        Ion Transport Mechanism (ScienceDirect)
      </div>
    </div>

    <!-- Right: Tech Specs -->
    <div class="space-y-8">
      <h3 class="text-4xl font-bold text-teal-400 mb-6">核心结构升级</h3>
      
      <div class="space-y-6">
        <div class="group bg-gray-800/50 p-6 rounded-xl border border-gray-700 hover:border-teal-500 transition cursor-default" v-motion-slide-visible-right>
          <div class="flex justify-between items-center mb-2">
            <div class="font-bold text-xl text-white">新型隔膜 (Zirfon)</div>
            <div class="i-carbon-chemistry text-teal-400 text-2xl"></div>
          </div>
          <p class="text-sm text-gray-400">复合膜替代石棉，阻抗降低 <b>50%</b>，实现零极距设计。</p>
        </div>

        <div class="group bg-gray-800/50 p-6 rounded-xl border border-gray-700 hover:border-teal-500 transition cursor-default" v-motion-slide-visible-right :delay="100">
           <div class="flex justify-between items-center mb-2">
            <div class="font-bold text-xl text-white">电流密度提升</div>
            <div class="i-carbon-flash text-teal-400 text-2xl"></div>
          </div>
          <p class="text-sm text-gray-400">从 0.4 提升至 <b>0.6 A/cm²</b>，同体积产能增加。</p>
        </div>
      </div>
    </div>
  </div>
</div>

---
layout: default
---

<!-- Slide 7: ALK Specs -->
# ALK 核心指标 (2025)
### Key Performance Indicators

<div class="grid grid-cols-3 gap-8 mt-16">
  <div class="relative group" v-motion-slide-visible-bottom>
    <div class="absolute inset-0 bg-teal-500/20 blur-xl rounded-full opacity-0 group-hover:opacity-100 transition duration-500"></div>
    <div class="relative text-center p-8 bg-gray-800/80 rounded-2xl border-t-4 border-teal-500 backdrop-blur-sm hover:-translate-y-2 transition duration-300">
      <div class="text-6xl font-black text-white mb-4">60%</div>
      <div class="text-teal-400 font-bold text-lg">System Efficiency</div>
      <div class="text-xs opacity-50 mt-2 border-t border-gray-700 pt-2">LHV Basis</div>
    </div>
  </div>

  <div class="relative group" v-motion-slide-visible-bottom :delay="100">
    <div class="absolute inset-0 bg-teal-500/20 blur-xl rounded-full opacity-0 group-hover:opacity-100 transition duration-500"></div>
    <div class="relative text-center p-8 bg-gray-800/80 rounded-2xl border-t-4 border-teal-500 backdrop-blur-sm hover:-translate-y-2 transition duration-300">
      <div class="text-6xl font-black text-white mb-4">0.6</div>
      <div class="text-teal-400 font-bold text-lg">A/cm²</div>
      <div class="text-xs opacity-50 mt-2 border-t border-gray-700 pt-2">Current Density</div>
    </div>
  </div>

  <div class="relative group" v-motion-slide-visible-bottom :delay="200">
    <div class="absolute inset-0 bg-teal-500/20 blur-xl rounded-full opacity-0 group-hover:opacity-100 transition duration-500"></div>
    <div class="relative text-center p-8 bg-gray-800/80 rounded-2xl border-t-4 border-teal-500 backdrop-blur-sm hover:-translate-y-2 transition duration-300">
      <div class="text-6xl font-black text-white mb-4">$300</div>
      <div class="text-teal-400 font-bold text-lg">Per kW</div>
      <div class="text-xs opacity-50 mt-2 border-t border-gray-700 pt-2">CAPEX (China)</div>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 8: PEM Visual Intro -->
<div class="w-full h-full bg-black relative overflow-hidden group">
  <img src="https://www.researchgate.net/figure/PEM-electrolyzer-experimental-setup_fig1_245349861" 
       class="absolute inset-0 w-full h-full object-contain bg-white p-20 opacity-80 group-hover:scale-110 transition duration-[2000ms]"
       style="view-transition-name: pem-img" />
  
  <div class="absolute inset-0 bg-blue-900/30 mix-blend-multiply"></div>
  
  <div class="absolute inset-0 flex items-center justify-center">
    <div class="relative">
      <div class="absolute -inset-10 bg-blue-500/30 blur-3xl rounded-full"></div>
      <h1 class="relative text-[10rem] font-black text-white tracking-tighter drop-shadow-2xl" v-motion-pop>
        PEM
      </h1>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 9: PEM Response -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden flex">
  <!-- Text on Left -->
  <div class="w-1/2 h-full flex flex-col justify-center px-12 z-10">
    <div class="flex items-center gap-4 mb-6">
      <div class="w-12 h-1 bg-blue-500"></div>
      <div class="text-blue-400 font-mono">FLEXIBILITY</div>
    </div>
    <h2 class="text-5xl font-bold text-white mb-8 leading-tight" v-motion-slide-visible-left>
      The Agile<br>Responder
    </h2>
    <p class="text-xl text-gray-300 leading-relaxed mb-8" v-motion-slide-visible-left :delay="100">
      面对风光发电的<b>毫秒级波动</b>，PEM 是唯一的全能选手。
    </p>
    
    <div class="bg-blue-900/20 border border-blue-500/30 p-6 rounded-xl" v-motion-slide-visible-left :delay="200">
      <div class="flex justify-between items-end">
        <div>
          <div class="text-4xl font-bold text-blue-400">0-100%</div>
          <div class="text-sm text-gray-400 mt-1">Load Range</div>
        </div>
        <div class="text-right">
          <div class="text-4xl font-bold text-blue-400">< 1s</div>
          <div class="text-sm text-gray-400 mt-1">Response Time</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Image moves to right half -->
  <div class="w-1/2 h-full relative bg-white">
    <img src="https://www.researchgate.net/figure/PEM-electrolyzer-experimental-setup_fig1_245349861" 
         class="absolute inset-0 w-full h-full object-contain p-10"
         style="view-transition-name: pem-img" />
    <div class="absolute inset-0 bg-gradient-to-l from-gray-900 via-gray-900/20 to-transparent"></div>
  </div>
</div>

---
layout: none
---

<!-- Slide 10: PEM Material (The Problem) -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden flex items-center justify-center">
  <!-- Background Elements -->
  <div class="absolute inset-0 grid grid-cols-12 gap-4 opacity-10 pointer-events-none">
    <div v-for="i in 12" :key="i" class="h-full w-full border-r border-blue-500/30"></div>
  </div>

  <div class="relative z-10 flex gap-16 items-center">
    <!-- Simulated Zoom into Catalyst -->
    <div class="relative w-[400px] h-[400px] rounded-full overflow-hidden border-4 border-blue-500 shadow-[0_0_80px_rgba(59,130,246,0.4)] bg-white group" v-motion-pop>
      <div class="absolute inset-0 bg-gray-200 flex items-center justify-center group-hover:scale-110 transition duration-700">
        <div class="text-center">
          <div class="text-6xl mb-2">💎</div>
          <span class="text-black font-bold text-2xl">IrO₂</span>
        </div>
      </div>
    </div>
    
    <!-- Info Card -->
    <div class="w-[500px]">
      <h3 class="text-4xl font-bold text-red-400 mb-6">The Iridium Bottleneck</h3>
      <ul class="space-y-6">
        <li class="flex items-start" v-motion-slide-visible-right>
          <div class="bg-red-500/20 p-2 rounded mr-4 text-red-400">⚠️</div>
          <div>
            <div class="font-bold text-white text-xl">Scarcity</div>
            <div class="text-gray-400">One of the rarest elements on Earth.</div>
          </div>
        </li>
        <li class="flex items-start" v-motion-slide-visible-right :delay="100">
          <div class="bg-red-500/20 p-2 rounded mr-4 text-red-400">💰</div>
          <div>
            <div class="font-bold text-white text-xl">Cost Impact</div>
            <div class="text-gray-400">Keeps CAPEX high ($800-1200/kW).</div>
          </div>
        </li>
        <li class="flex items-start" v-motion-slide-visible-right :delay="200">
          <div class="bg-green-500/20 p-2 rounded mr-4 text-green-400">💡</div>
          <div>
            <div class="font-bold text-white text-xl">Solution</div>
            <div class="text-gray-400">Nanostructured catalysts reduce loading to <b>0.5 mg/cm²</b>.</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</div>

---
layout: default
---

<!-- Slide 11: PEM Specs -->
# PEM 核心指标 (2025)
### Key Performance Indicators

<div class="grid grid-cols-3 gap-8 mt-16">
  <div class="relative group" v-motion-slide-visible-bottom>
    <div class="absolute inset-0 bg-blue-500/20 blur-xl rounded-full opacity-0 group-hover:opacity-100 transition duration-500"></div>
    <div class="relative text-center p-8 bg-gray-800/80 rounded-2xl border-t-4 border-blue-500 backdrop-blur-sm hover:-translate-y-2 transition duration-300">
      <div class="text-6xl font-black text-white mb-4">2.0</div>
      <div class="text-blue-400 font-bold text-lg">A/cm²</div>
      <div class="text-xs opacity-50 mt-2 border-t border-gray-700 pt-2">High Current Density</div>
    </div>
  </div>

  <div class="relative group" v-motion-slide-visible-bottom :delay="100">
    <div class="absolute inset-0 bg-blue-500/20 blur-xl rounded-full opacity-0 group-hover:opacity-100 transition duration-500"></div>
    <div class="relative text-center p-8 bg-gray-800/80 rounded-2xl border-t-4 border-blue-500 backdrop-blur-sm hover:-translate-y-2 transition duration-300">
      <div class="text-6xl font-black text-white mb-4">50k</div>
      <div class="text-blue-400 font-bold text-lg">Hours</div>
      <div class="text-xs opacity-50 mt-2 border-t border-gray-700 pt-2">Lifetime</div>
    </div>
  </div>

  <div class="relative group" v-motion-slide-visible-bottom :delay="200">
    <div class="absolute inset-0 bg-blue-500/20 blur-xl rounded-full opacity-0 group-hover:opacity-100 transition duration-500"></div>
    <div class="relative text-center p-8 bg-gray-800/80 rounded-2xl border-t-4 border-blue-500 backdrop-blur-sm hover:-translate-y-2 transition duration-300">
      <div class="text-6xl font-black text-white mb-4">$800</div>
      <div class="text-blue-400 font-bold text-lg">Per kW</div>
      <div class="text-xs opacity-50 mt-2 border-t border-gray-700 pt-2">CAPEX (Global)</div>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 12: Fukushima Aerial -->
<div class="w-full h-full relative">
  <img src="https://www.japan.go.jp/kizuna/_src/7989315/hydrogen-production_facility_01.jpg?v=1760945198119" 
       class="absolute inset-0 w-full h-full object-cover"
       style="view-transition-name: fukushima-img" />
  
  <div class="absolute bottom-12 left-12 bg-black/70 p-6 rounded-xl backdrop-blur-md">
    <h2 class="text-4xl font-bold text-white">Fukushima FH2R</h2>
    <p class="text-gray-300">10MW Class Renewable Hydrogen Production</p>
  </div>
</div>

---
layout: none
---

<!-- Slide 13: The Challenge (Blur) -->
<div class="w-full h-full relative bg-black">
  <img src="https://www.japan.go.jp/kizuna/_src/7989315/hydrogen-production_facility_01.jpg?v=1760945198119" 
       class="absolute inset-0 w-full h-full object-cover opacity-40 blur-sm scale-110 transition duration-1000"
       style="view-transition-name: fukushima-img" />
  
  <div class="absolute inset-0 flex items-center justify-center">
    <div class="text-center">
      <h1 class="text-6xl font-bold text-red-500 mb-4" v-motion-pop>Intermittency</h1>
      <p class="text-2xl text-white max-w-3xl">
        Solar power fluctuates wildly.<br>
        Direct coupling kills electrolyzers.
      </p>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 14: The Solution (Move Top) -->
<div class="w-full h-full bg-gray-900 relative flex flex-col">
  <!-- Image moves to top banner -->
  <div class="h-1/3 relative overflow-hidden">
    <img src="https://www.japan.go.jp/kizuna/_src/7989315/hydrogen-production_facility_01.jpg?v=1760945198119" 
         class="absolute inset-0 w-full h-full object-cover"
         style="view-transition-name: fukushima-img" />
    <div class="absolute inset-0 bg-black/20"></div>
    <div class="absolute bottom-4 left-8 text-white font-bold text-2xl">Solution Architecture</div>
  </div>

  <!-- Diagram Area -->
  <div class="h-2/3 p-12 flex gap-8">
    <div class="flex-1 bg-gray-800 rounded-xl p-6 border border-yellow-500/30" v-motion-slide-visible-bottom>
      <h3 class="text-yellow-400 font-bold mb-4">1. Battery Buffer</h3>
      <p class="text-sm opacity-70">Li-ion batteries smooth out second-level fluctuations.</p>
    </div>
    <div class="flex-1 bg-gray-800 rounded-xl p-6 border border-yellow-500/30" v-motion-slide-visible-bottom :delay="100">
      <h3 class="text-yellow-400 font-bold mb-4">2. Wide-Range ALK</h3>
      <p class="text-sm opacity-70">Modified ALK stacks capable of 5-120% load operation.</p>
    </div>
    <div class="flex-1 bg-gray-800 rounded-xl p-6 border border-yellow-500/30" v-motion-slide-visible-bottom :delay="200">
      <h3 class="text-yellow-400 font-bold mb-4">3. Predictive Control</h3>
      <p class="text-sm opacity-70">AI forecasts solar output 15 mins ahead.</p>
    </div>
  </div>
</div>

---
layout: default
---

<!-- Slide 15: Result -->
# 运行成效
### Operational Results

<div class="flex justify-center items-center h-full pb-20">
  <div class="relative w-[800px] h-[400px] bg-gray-800 rounded-xl border border-gray-700 flex items-center justify-center">
    <div class="text-center">
      <div class="text-6xl font-bold text-green-400 mb-4">Stable Output</div>
      <div class="text-2xl text-white">Even during cloud cover</div>
      <div class="mt-8 flex gap-4 justify-center">
        <span class="px-4 py-2 bg-green-900/50 rounded text-green-300">Grid Balancing</span>
        <span class="px-4 py-2 bg-green-900/50 rounded text-green-300">H2 Quality > 99.99%</span>
      </div>
    </div>
  </div>
</div>

---
layout: none
---

<!-- Slide 16: Offshore Vision -->
<div class="w-full h-full relative">
  <img src="https://www.nrel.gov/images/libraries/news/program/2024/20240715-offshore-wind-turbines-offer-path-for-clean-hydrogen-production-84771.jpg?sfvrsn=60d0f078_0" 
       class="absolute inset-0 w-full h-full object-cover"
       style="view-transition-name: offshore-img" />
  
  <div class="absolute top-12 right-12 text-right">
    <h1 class="text-7xl font-black text-white drop-shadow-lg">OFFSHORE</h1>
    <h2 class="text-3xl font-light text-blue-200">The Next Frontier</h2>
  </div>
</div>

---
layout: none
---

<!-- Slide 17: Offshore Deep Dive (Move Left) -->
<div class="w-full h-full bg-blue-950 relative overflow-hidden flex">
  <!-- Image moves left -->
  <div class="w-1/2 h-full relative">
    <img src="https://www.nrel.gov/images/libraries/news/program/2024/20240715-offshore-wind-turbines-offer-path-for-clean-hydrogen-production-84771.jpg?sfvrsn=60d0f078_0" 
         class="absolute inset-0 w-full h-full object-cover opacity-80"
         style="view-transition-name: offshore-img" />
  </div>

  <!-- Content Right -->
  <div class="w-1/2 h-full p-12 flex flex-col justify-center">
    <h2 class="text-4xl font-bold text-white mb-8">Why go deep?</h2>
    <ul class="space-y-6">
      <li class="flex items-center text-xl text-blue-200" v-motion-slide-visible-right>
        <carbon:arrow-right class="mr-4"/> Higher Wind Speeds (>10m/s)
      </li>
      <li class="flex items-center text-xl text-blue-200" v-motion-slide-visible-right :delay="100">
        <carbon:arrow-right class="mr-4"/> Unlimited Space
      </li>
      <li class="flex items-center text-xl text-blue-200" v-motion-slide-visible-right :delay="200">
        <carbon:arrow-right class="mr-4"/> <b>Pipeline vs Cable</b>: <br>H2 transport is cheaper > 100km
      </li>
    </ul>
  </div>
</div>

---
layout: default
---

<!-- Slide 18: Offshore Challenges -->
# 工程挑战：严酷环境
### Harsh Environments

<div class="grid grid-cols-3 gap-8 mt-12">
  <div class="bg-red-900/20 p-8 rounded-xl border border-red-500/50 hover:bg-red-900/40 transition">
    <div class="text-4xl mb-4">🧂</div>
    <h3 class="text-xl font-bold text-red-400">Salt Spray</h3>
    <p class="text-sm mt-2 opacity-70">Corrosion of electronics and electrodes.</p>
  </div>
  <div class="bg-red-900/20 p-8 rounded-xl border border-red-500/50 hover:bg-red-900/40 transition">
    <div class="text-4xl mb-4">🌊</div>
    <h3 class="text-xl font-bold text-red-400">Motion</h3>
    <p class="text-sm mt-2 opacity-70">Wave motion disrupts gas-liquid separation.</p>
  </div>
  <div class="bg-red-900/20 p-8 rounded-xl border border-red-500/50 hover:bg-red-900/40 transition">
    <div class="text-4xl mb-4">🔧</div>
    <h3 class="text-xl font-bold text-red-400">O&M</h3>
    <p class="text-sm mt-2 opacity-70">Maintenance costs are 3-5x higher than onshore.</p>
  </div>
</div>

---
layout: section
---

<!-- Slide 19: Academic Section Intro -->
<div class="absolute inset-0 bg-gradient-to-r from-gray-900 via-purple-900/50 to-gray-900 z-0"></div>
<div class="relative z-10 text-center">
  <h1 class="text-6xl font-bold text-purple-400 drop-shadow-lg">ACADEMIC FRONTIERS</h1>
  <p class="text-xl mt-4 opacity-80 tracking-widest">PART 02</p>
</div>

---
layout: none
---

<!-- Slide 20: AEM Visual -->
<div class="w-full h-full bg-black relative overflow-hidden flex items-center justify-center">
  <img src="https://pub.mdpi-res.com/membranes/membranes-12-00173/article_deploy/html/images/membranes-12-00173-g001.png?1644467578" 
       class="w-3/4 h-3/4 object-contain bg-white/10 rounded-xl backdrop-blur-sm p-4"
       style="view-transition-name: aem-img" />
  
  <div class="absolute bottom-12 text-center">
    <h2 class="text-5xl font-bold text-purple-400">AEM</h2>
    <p class="text-white">The Hybrid Solution</p>
  </div>
</div>

---
layout: none
---

<!-- Slide 21: AEM Innovation (Move Right) -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden flex">
  <div class="w-1/2 h-full p-12 flex flex-col justify-center">
    <h2 class="text-4xl font-bold text-purple-400 mb-6">Best of Both Worlds</h2>
    <div class="space-y-4">
      <div class="p-4 bg-purple-900/30 rounded-lg border-l-4 border-purple-500">
        <div class="font-bold text-white">Low Cost (Like ALK)</div>
        <div class="text-sm opacity-70">Uses Ni/Fe catalysts. No Iridium.</div>
      </div>
      <div class="p-4 bg-blue-900/30 rounded-lg border-l-4 border-blue-500">
        <div class="font-bold text-white">High Performance (Like PEM)</div>
        <div class="text-sm opacity-70">High current density & pressure.</div>
      </div>
    </div>
  </div>

  <div class="w-1/2 h-full flex items-center justify-center bg-black/20">
    <img src="https://pub.mdpi-res.com/membranes/membranes-12-00173/article_deploy/html/images/membranes-12-00173-g001.png?1644467578" 
         class="w-3/4 object-contain bg-white/10 rounded-xl p-4"
         style="view-transition-name: aem-img" />
  </div>
</div>

---
layout: none
---

<!-- Slide 22: Seawater Dream -->
<div class="w-full h-full bg-blue-900 relative overflow-hidden">
  <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1468581264429-2548ef9eb732?q=80&w=2074&auto=format&fit=crop')] bg-cover bg-center opacity-60"></div>
  
  <div class="absolute inset-0 flex items-center justify-center">
    <h1 class="text-8xl font-black text-white drop-shadow-2xl tracking-widest">SEAWATER</h1>
  </div>
</div>

---
layout: none
---

<!-- Slide 23: Seawater Prototype (Center) -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden flex items-center justify-center">
  <img src="https://en.szu.edu.cn/__local/0/3E/E8/31F3209732FD18866B8474BD011_18AD6139_68D59.png?e=.png" 
       class="w-[600px] rounded-xl shadow-[0_0_50px_rgba(59,130,246,0.4)]"
       style="view-transition-name: seawater-img" />
  
  <div class="absolute bottom-20 text-center">
    <div class="bg-black/60 px-6 py-2 rounded-full text-white">Shenzhen University Prototype</div>
  </div>
</div>

---
layout: none
---

<!-- Slide 24: Seawater Mechanism (Move Left) -->
<div class="w-full h-full bg-gray-900 relative overflow-hidden flex">
  <div class="w-1/2 h-full flex items-center justify-center bg-black/20">
    <img src="https://en.szu.edu.cn/__local/0/3E/E8/31F3209732FD18866B8474BD011_18AD6139_68D59.png?e=.png" 
         class="w-[400px] rounded-xl shadow-lg"
         style="view-transition-name: seawater-img" />
  </div>

  <div class="w-1/2 h-full p-12 flex flex-col justify-center">
    <h2 class="text-3xl font-bold text-blue-400 mb-6">Phase Migration Mechanism</h2>
    <div class="bg-gray-800 p-6 rounded-xl border border-gray-700">
      <p class="text-sm leading-relaxed text-gray-300">
        <span class="text-teal-400 font-bold">The Breakthrough:</span><br>
        Creating a "freshwater layer" in-situ via a hydrophobic membrane.
        <br><br>
        Water vapor permeates, but liquid seawater (and Cl⁻ ions) are blocked.
      </p>
      <div class="mt-4 h-32 bg-black/40 rounded border border-dashed border-gray-600 flex items-center justify-center">
        <span class="text-xs opacity-40">Mechanism Diagram</span>
      </div>
    </div>
  </div>
</div>

---
layout: end
---

# 感谢聆听
## Q & A

<div class="mt-12 text-sm opacity-60 font-mono">
  PPT Design powered by Slidev & UnoCSS
</div>