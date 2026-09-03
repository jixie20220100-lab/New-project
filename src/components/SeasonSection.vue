<script setup>
const features = [
  { number: '01', label: '新区域', title: '熔火峡谷', action: 'EXPLORE →', tone: 'cyan' },
  { number: '02', label: '新模式', title: '核心争夺', action: 'PLAY NOW →', tone: 'orange' },
  { number: '03', label: '新英雄', title: '赛拉 · 余烬', action: 'MEET SERA →', tone: 'violet' },
]
</script>

<template>
  <section id="season" class="season">
    <div class="section-heading">
      <p class="eyebrow"><span></span> 第 03 赛季</p>
      <h2>边境之<span>焰</span></h2>
      <p>探索全新区域、武器与限时玩法。</p>
    </div>
    <div class="feature-grid">
      <article v-for="feature in features" :key="feature.number" class="feature-card" :class="feature.tone">
        <p>{{ feature.number }} / {{ feature.label }}</p>
        <h3>{{ feature.title }}</h3>
        <span>{{ feature.action }}</span>
      </article>
    </div>
  </section>
</template>
