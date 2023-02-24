<script setup lang="ts">
// @ts-ignore
import Projects from '../components/Projects/Projects.vue'
import Meetings from '../components/Meetings/Meetings.vue'
</script>

<template>
  <div class="grid md:grid-cols-2 gap-[25px] w-full">
    <Projects />
    <Meetings />
  </div>
</template>
