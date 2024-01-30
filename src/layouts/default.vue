<!--
 @name: default.vue
 @description: 
 @author: 程序员优雅哥 yygcoder
 @time: 2024/1/30 20:13
-->
<template>
  <div class="default">
    <div>header</div>
    <router-view></router-view>
    <div>footer</div>
  </div>
</template>

<script setup lang="ts">
console.log('default')
</script>

<style scoped>
.default {
}
</style>
