<template>
  <aside class="sidebar">
    <div class="logo"><Logo class="logo-icon" /></div>

    <nav class="nav-links">
      <SidebarItem :icon="HomeIcon" text="Home" @click="$emit('changeView', 'default')" />
      <SidebarItem
        :icon="SessionsIcon"
        text="View sessions"
        :showArrow="true"
        @click="$emit('changeView', 'default')"
      />
      <SidebarItem :icon="PatientIcon" text="Patient records" active />
      <SidebarItem :icon="MediaIcon" text="Media" @click="$emit('changeView', 'default')" />
      <SidebarItem
        :icon="ConsultIcon"
        text="Virtual consultation"
        @click="$emit('changeView', 'default')"
      />
      <SidebarItem :icon="StatsIcon" text="Statistics" @click="$emit('changeView', 'default')" />
    </nav>

    <div class="user-card">
      <div class="avatar">RL</div>
      <div class="info">
        <span>Robert Lindley</span>
        <small>robertlindley@sho...</small>
      </div>
      <div class="arrow"><span class="material-symbols-outlined"> chevron_right </span></div>
    </div>
  </aside>
</template>

<script setup>
import SidebarItem from './SidebarItem.vue'

import Logo from '@/assets/Logo.svg'
import HomeIcon from '@/assets/icons/sideBar/home.svg'
import SessionsIcon from '@/assets/icons/sideBar/sessions.svg'
import PatientIcon from '@/assets/icons/sideBar/patient.svg'
import MediaIcon from '@/assets/icons/sideBar/media.svg'
import ConsultIcon from '@/assets/icons/sideBar/consult.svg'
import StatsIcon from '@/assets/icons/sideBar/stats.svg'
</script>
