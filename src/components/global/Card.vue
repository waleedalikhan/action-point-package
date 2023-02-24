<script setup lang="ts">
import { defineProps } from 'vue'
import cn from 'classnames'

const props = defineProps<{ class?: string }>()
</script>

<template>
  <div :class="cn('card-container p-5 w-full', props.class)">
    <slot />
  </div>
</template>

<style scoped>
.card-container {
  border-radius: 20px;
  border: 1px solid rgba(228, 228, 228, 1);
  box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.5) inset;
}
</style>
