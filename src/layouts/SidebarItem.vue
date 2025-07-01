<template>
  <div class="sidebar-item" :class="{ active }">
    <component :is="icon" class="icon" />
    <span class="text">{{ text }}</span>
    <span v-if="showArrow" class="arrow material-symbols-outlined arrow">chevron_right</span>
  </div>
</template>

<script setup>
defineProps({
  icon: Object,
  text: String,
  active: Boolean,
  showArrow: Boolean,
})
</script>
