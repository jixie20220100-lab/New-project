<script setup>
import { onBeforeUnmount, ref } from 'vue'
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import SeasonSection from './components/SeasonSection.vue'
import ToastMessage from './components/ToastMessage.vue'

const toastVisible = ref(false)
let toastTimer

function startGame() {
  window.clearTimeout(toastTimer)
  toastVisible.value = true
  toastTimer = window.setTimeout(() => {
    toastVisible.value = false
  }, 2600)
}

onBeforeUnmount(() => window.clearTimeout(toastTimer))
</script>

<template>
  <main class="page-shell">
    <NavBar />
    <HeroSection @start-game="startGame" />
    <SeasonSection />
  </main>
  <ToastMessage :visible="toastVisible" />
</template>
