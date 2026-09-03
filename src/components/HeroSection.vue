<script setup>
defineEmits(['start-game'])
</script>

<template>
  <section id="top" class="hero">
    <div class="sun" aria-hidden="true"></div>
    <div class="grid" aria-hidden="true"></div>
    <div class="orb orb-one" aria-hidden="true"></div>
    <div class="orb orb-two" aria-hidden="true"></div>
    <div class="hero-copy">
      <p class="eyebrow"><span></span> 新赛季现已开启</p>
      <h1>踏入未知<br /><em>燃起你的光</em></h1>
      <p class="intro">在坠落的霓虹都市中组建小队，夺取最后的能源核心。<br />每一次选择，都将改写边境的秩序。</p>
      <div class="hero-actions">
        <button class="primary-button" type="button" @click="$emit('start-game')"><span>▶</span> 立即开始</button>
        <a class="watch-link" href="#season"><i>▶</i> 观看赛季预告</a>
      </div>
    </div>
    <div class="hero-art" aria-label="机甲战士概念插画">
      <div class="fighter"><div class="helmet"><span></span></div><div class="torso"></div><div class="arm arm-left"></div><div class="arm arm-right"></div><div class="weapon"></div></div>
      <div class="art-caption">UNIT 09<br /><b>PHANTOM</b></div>
    </div>
    <div class="scroll-hint">SCROLL TO EXPLORE <span></span></div>
  </section>
</template>
