<!--
 @name: default.vue
 @description: 
 @author: 程序员优雅哥 yygcoder
 @time: 2024/1/30 20:13
-->
<template>
  <div class="default">
    <div class="flex">
      <router-link to="/">首页</router-link>
      <router-link to="/about">about</router-link>
    </div>
    <router-view></router-view>
    <div>footer</div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.default {
}
</style>
