<template>
  <div class="default-view">
    <img src="@/assets/icons/working.gif" alt="In Progress" class="progress-gif" />
    <p>This section is still in progress</p>
    <button class="go-btn" @click="$emit('goToPatient')">Back to Patient Records</button>
  </div>
</template>

<script setup>
defineEmits(['goToPatient'])
</script>
