<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps<{ btnText: string }>()
</script>

<template>
  <button
    class="sidebar-btn w-full h-[38px] flex items-center justify-center uppercase text-title text-xs font-poppins font-medium outline-none focus:outline-none"
  >
    {{ props.btnText }}
  </button>
</template>

<style scoped>
.sidebar-btn {
  border-radius: 19px;
  border: 1px solid rgba(228, 228, 228, 1);
}
</style>
