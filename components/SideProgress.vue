<template>
  <div v-if="currentTopic" class="fixed right-4 top-1/2 transform -translate-y-1/2 z-50 flex flex-col items-end gap-3 pointer-events-none">
    <div v-for="(item, index) in topics" :key="item.key"
         class="flex items-center gap-3 transition-all duration-500 group"
         :class="getItemClass(index)">
      
      <!-- Label -->
      <span class="text-[10px] font-bold tracking-widest uppercase transition-all duration-300" 
            :class="getLabelClass(index)">
        {{ item.label }}
      </span>
      
      <!-- Dot/Bar -->
      <div class="w-1.5 h-1.5 rounded-full transition-all duration-300"
           :class="getDotClass(index)"></div>
           
      <!-- Connecting Line (visual only, maybe pseudo-element better but this is simple) -->
      <!-- <div v-if="index < topics.length - 1" class="absolute right-[5px] top-[14px] w-[1px] h-[12px] bg-white/10 -z-10"></div> -->
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

const { currentSlideRoute } = useNav()

const topics = [
  { key: 'intro', label: '原理' },
  { key: 'alk', label: 'ALK' },
  { key: 'pem', label: 'PEM' },
  { key: 'aem', label: 'AEM' },
  { key: 'seawater', label: '海水' },
  { key: 'offshore', label: '离岸' },
  { key: 'pec', label: 'PEC' },
  { key: 'future', label: '展望' },
]

const currentTopic = computed(() => currentSlideRoute.value.meta?.frontmatter?.topic)
const currentIndex = computed(() => topics.findIndex(t => t.key === currentTopic.value))

function getItemClass(index: number) {
  if (currentIndex.value === -1) return 'opacity-0' 
  if (index === currentIndex.value) return 'opacity-100 scale-105'
  if (index < currentIndex.value) return 'opacity-40'
  return 'opacity-20'
}

function getLabelClass(index: number) {
  if (index === currentIndex.value) return 'text-teal-400 translate-x-0'
  return 'text-white translate-x-4 opacity-0 group-hover:opacity-100 group-hover:translate-x-0'
}

function getDotClass(index: number) {
  if (index === currentIndex.value) return 'bg-teal-400 w-2 h-2 shadow-[0_0_10px_rgba(45,212,191,0.8)]'
  if (index < currentIndex.value) return 'bg-white'
  return 'bg-white/50'
}
</script>
