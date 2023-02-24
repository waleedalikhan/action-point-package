<template>
  <div class="xl:container mx-auto xl:pr-0 lg:pr-6 pr-4 xl:pt-0 pt-10">
    <div class="flex gap-[25px] py-8 items-start">
      <Sidebar />
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
// @ts-ignore
import Sidebar from './Sidebar/Sidebar.vue'
</script>

<style></style>
