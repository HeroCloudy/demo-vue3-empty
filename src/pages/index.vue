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

    <!-- A basic anchor icon from Phosphor icons -->
    <div class="i-ph-anchor-simple-thin" />
    <!-- An orange alarm from Material Design Icons -->
    <div class="i-mdi-alarm text-orange-400" />
    <!-- A large Vue logo -->
    <div class="i-logos-vue text-3xl" />
    <!-- Sun in light mode, Moon in dark mode, from Carbon -->
    <button class="i-carbon-sun dark:i-carbon-moon" />
    <!-- Twemoji of laugh, turns to tear on hovering -->
    <div class="i-twemoji-grinning-face-with-smiling-eyes hover:i-twemoji-face-with-tears-of-joy" />

    <!-- custom -->
    <div class="i-ic:baseline-4g-plus-mobiledata w-2em h-2em" style="color: red"></div>

    <!--    <ReloadPrompt></ReloadPrompt>-->

    <!--    <div>hello</div>-->
  </div>
</template>

<script setup lang="ts">
import { useRegisterSW } from 'virtual:pwa-register/vue'

const intervalMS = 5 * 1000

onMounted(() => {
  useRegisterSW({
    immediate: true,
    // onNeedRefresh() {
    //   console.log('need refresh')
    // },
    onRegisteredSW(_url, registration) {
      // console.log(url, registration)
      registration &&
        setInterval(() => {
          registration.update()
        }, intervalMS)
    }
  })
})
// defineOptions({
//   name: 'HomeIndex'
// })

// defineRender(() => <div>Hello</div>)

const msg = ref('hello world')

const target = ref(null)

const { x, y, isOutside } = useMouseInElement(target)
</script>

<style scoped></style>
<route lang="yaml">
meta:
  layout: default
</route>
