<!--
 @name: index.vue
 @description: 
 @author: 程序员优雅哥 yygcoder
 @time: 2024/1/28 23:30
-->
<template>
  <div ref="target">
    <router-link to="/">home</router-link>
    <router-link to="/about">about</router-link>
    <div>{{ msg }}</div>
    <div class="text-3xl font-bold underline">hello world</div>

    <p>x: {{ x }}</p>
    <p>y: {{ y }}</p>
    <p>isOutSide: {{ isOutside }}</p>

    <hello-world msg="Hello world Component"></hello-world>
  </div>
</template>

<script setup lang="ts">
const msg = ref('hello world')

const target = ref(null)

const { x, y, isOutside } = useMouseInElement(target)
</script>

<style scoped></style>
