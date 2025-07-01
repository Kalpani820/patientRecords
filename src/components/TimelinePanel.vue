// TimelinePanel.vue
<template>
  <div class="timeline-panel">
    <div :class="['expand-arrow', { 'inside-timeline': isOpen }]" @click="$emit('toggle')">
      <span v-if="!isOpen" class="material-symbols-outlined">keyboard_double_arrow_right</span>
      <span v-else class="material-symbols-outlined">keyboard_double_arrow_left</span>
    </div>

    <aside v-if="isOpen" class="timeline">
      <h3>Timeline</h3>
      <ul>
        <TimelineItem time="09:45 AM" icon="consentSignIn" title="Consent form signed" />

        <TimelineItem
          time="09:45 AM"
          icon="treatment"
          title="3 treatments chosen"
          :subItems="['Root canal', 'Dental extraction', 'Teeth whitening']"
        />

        <TimelineItem
          time="3 July, 16:15 PM"
          icon="send"
          title="Bundle 2 sent"
          meta="johnsmith@gmail.com"
        />

        <TimelineItem
          time="3 July, 16:15 PM"
          icon="send"
          title="Bundle 2 sent"
          meta="johnsmith@gmail.com"
        />

        <TimelineItem
          time="3 July, 17:15 PM"
          icon="consentReject"
          title="Consent form declined"
          meta="johnsmith@gmail.com"
        />

        <!-- Add more -->
      </ul>
    </aside>
  </div>
</template>

<script setup>
import TimelineItem from './TimelineItem.vue'

defineProps({
  isOpen: Boolean,
})
defineEmits(['toggle'])
</script>
