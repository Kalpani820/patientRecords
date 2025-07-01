<!-- TimelineItem.vue -->
<template>
  <li class="timeline-item">
    <div class="icon-text">
      <div class="icon-wrapper" :class="iconClass">
        <component :is="getIcon(icon)" />
      </div>
      <div class="content">
        <span class="time">{{ time }}</span>
        <strong>{{ title }}</strong>
        <div v-if="meta" class="meta">{{ meta }}</div>
        <ul v-if="subItems?.length" class="sub">
          <li v-for="(item, idx) in subItems" :key="idx">{{ item }}</li>
        </ul>
      </div>
    </div>
  </li>
</template>

<script setup>
import ConsentRejectIcon from '@/assets/icons/timeline/consentReject.svg'
import TreatmentIcon from '@/assets/icons/timeline/treatment.svg'
import ConsentSigninIcon from '@/assets/icons/timeline/consentSignIn.svg'
import SendIcon from '@/assets/icons/timeline/send.svg'

defineProps({
  time: String,
  icon: String,
  title: String,
  meta: String,
  subItems: Array,
})

const getIcon = (type) => {
  switch (type) {
    case 'consentReject':
      return ConsentRejectIcon
    case 'treatment':
      return TreatmentIcon
    case 'consentSignIn':
      return ConsentSigninIcon
    case 'send':
      return SendIcon
    default:
      return null
  }
}
</script>
