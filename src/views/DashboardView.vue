<template>
  <div class="layout right-side">


    <button class="menu-toggle" @click="toggleSidebar">
      <span class="material-symbols-outlined">menu</span>
    </button>
    <Sidebar :class="{ open: isSidebarOpen }" @changeView="handleViewChange" />
    <div :class="['main-content-wrapper', { 'timeline-open': isTimelineOpen }]">
      <template v-if="selectedView === 'patient'">
        <main class="main-content">
           <div class="small-screen-header"></div>
          <BreadcrumbNav />
          <DetailsTabs />
          <PatientCard />
        </main>
        <TimelinePanel :isOpen="isTimelineOpen" @toggle="toggleTimeline" />
      </template>

      <template v-else>
        <!-- <div class="default-placeholder">
          <p>Please select a patient record to continue.</p>
          <button class="primary-btn" @click="selectedView = 'patient'">
            View Patient Records
          </button>
        </div> -->
        <DefaultView @goToPatient="selectedView = 'patient'" />
      </template>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Sidebar from '../layouts/SideBar.vue'
import BreadcrumbNav from '../components/BreadcrumbNav.vue'
import DetailsTabs from '../components/DetailsTabs.vue'
import PatientCard from '../components/PatientCard.vue'
import TimelinePanel from '../components/TimelinePanel.vue'
import DefaultView from '../components/DefaultView.vue'

const selectedView = ref('patient') // default or 'patient'

const isTimelineOpen = ref(false)
const isSidebarOpen = ref(false)

const toggleTimeline = () => {
  isTimelineOpen.value = !isTimelineOpen.value
}

// This will be passed down to sidebar to change view
const handleViewChange = (view) => {
  selectedView.value = view
  isSidebarOpen.value = false // auto-close on mobile
}



function toggleSidebar() {
  isSidebarOpen.value = !isSidebarOpen.value
}

</script>
