<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="layout">
    <RouterView />
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  height: 100vh;
  overflow: hidden;
}
</style>
