<template>
  <div class="tab-header">
    <div class="tab-actions">
      <div class="tabs">
        <button :class="{ active: selectedTab === 'note' }" @click="selectedTab = 'note'">
          Notes
        </button>
        <button :class="{ active: selectedTab === 'bundle' }">Bundles</button>
      </div>
      <button class="edit-btn">
        <span class="material-symbols-outlined">edit</span>
        Edit session
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const selectedTab = ref('note')
</script>
