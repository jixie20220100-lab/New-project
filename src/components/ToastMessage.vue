<script setup>
defineProps({
  visible: Boolean,
})
</script>

<template>
  <div class="toast" :class="{ show: visible }" role="status" aria-live="polite">
    正在为你连接边境服务器…
  </div>
</template>
