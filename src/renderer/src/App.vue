<template>
  <Suspense>
    <main class="">
      <Camera />
    </main>
  </Suspense>
</template>

<script setup lang="ts">
import Camera from './components/Camera.vue';
</script>

<style lang="less">
@import './assets/css/styles.less';
</style>
