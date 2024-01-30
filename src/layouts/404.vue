<!--
 @name: 404.vue
 @description: 
 @author: 程序员优雅哥 yygcoder
 @time: 2024/1/30 23:35
-->
<template>
  <div class="404">
    <h1>404 - 页面不存在</h1>
    <router-view></router-view>

    <button @click="$router.back()">返回</button>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
