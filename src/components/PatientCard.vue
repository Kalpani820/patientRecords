<template>
  <div class="patient-card custom-scroller">
    <div class="card-header">
      <span class="badge"><Template class="templeate-icon" />Template A</span>
      <div class="card-actions">
        <span class="badge"><Copy class="templeate-icon" /></span>
        <span class="badge"><Download class="templeate-icon" /></span>
      </div>
    </div>

    <h2 class="card-title">Notes</h2>
    <p class="last-updated">Last updated today 09:15 AM</p>

    <hr />

    <div class="field-group">
      <label>Dentist</label>
      <div>Dr John Smith</div>
    </div>

    <div class="field-group">
      <label for="nurse">Nurse</label>
      <input id="nurse" type="text" placeholder="Type here" />
    </div>

    <div class="field-group">
      <label>When did the fracture occur?</label>
      <div class="tag-group">
        <button class="tag">Today</button>
        <button class="tag selected">Yesterday</button>
        <button class="tag">Several days ago</button>
        <button class="tag">Over a week ago</button>
        <button class="tag">N/A</button>
      </div>
    </div>

    <div class="field-group with-tooltip">
      <label> Location of broken tooth </label>
      <div class="value with-hover-tooltip">
        Broken tooth lorem
        <div class="tooltip-bubble">
          <span class="material-symbols-outlined">info</span>
        </div>
      </div>
    </div>

    <div class="field-group">
      <label>Reason for attendance</label>
      <div class="value">Broken tooth lorem</div>
    </div>

    <div class="field-group">
      <label>When did the fracture occur?</label>
      <div class="value">Broken tooth</div>
    </div>

    <div class="field-group">
      <label>How did it happen?</label>
      <div class="value">Broken tooth</div>
    </div>
  </div>
</template>

<script setup>
import Template from '@/assets/icons/template.svg'
import Copy from '@/assets/icons/copy.svg'
import Download from '@/assets/icons/download.svg'
</script>
