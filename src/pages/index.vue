<!--
 @name: index.vue
 @description: 
 @author: 程序员优雅哥 yygcoder
 @time: 2024/1/28 23:30
-->
<template>
  <div>home</div>
</template>

<script setup lang="ts">
import { useRegisterSW } from 'virtual:pwa-register/vue'

const intervalMS = 60 * 60 * 1000

onMounted(() => {
  useRegisterSW({
    immediate: true,
    onRegisteredSW(_url, registration) {
      registration &&
        setInterval(() => {
          registration.update()
        }, intervalMS)
    }
  })
})
</script>

<style scoped></style>

<route lang="yaml">
meta:
  layout: default
</route>
