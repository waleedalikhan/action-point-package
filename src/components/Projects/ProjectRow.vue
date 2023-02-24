<script setup lang="ts">
import { defineProps } from 'vue'
import cn from 'classnames'

import CalendarIcon from '../global/icons/CalendarIcon.vue'
import PencilIcon from '../global/icons/PencilIcon.vue'
import DeleteIcon from '../global/icons/DeleteIcon.vue'

const props = defineProps<{
  date: string
  title: string
  desc: string
  isActive: boolean
  onRowClick?: () => void
}>()
</script>

<template>
  <div
    :class="
      cn('flex items-center cursor-pointer', {
        'project-row': !props.isActive,
        'active-project-row': props.isActive,
      })
    "
    @click="props.onRowClick"
  >
    <div
      :class="
        cn('p-4 rounded-l-[20px] h-[117px]', {
          'bg-light': !props.isActive,
          'bg-primary': props.isActive,
        })
      "
    >
      <div
        :class="
          cn('flex items-center space-x-2', {
            'text-secondary': !props.isActive,
            'text-white': props.isActive,
          })
        "
      >
        <div>
          <CalendarIcon />
        </div>
        <div>
          <p class="text-xs font-poppins font-light">{{ props.date }}</p>
        </div>
      </div>
      <button
        :class="
          cn(
            'flex items-center space-x-2 my-3 outline-none focus:outline-none',
            {
              'text-secondary': !props.isActive,
              'text-white': props.isActive,
            },
          )
        "
      >
        <span>
          <PencilIcon />
        </span>
        <span>
          <span class="text-xs font-poppins font-light">
            Edit
          </span>
        </span>
      </button>
      <button
        :class="
          cn('flex items-center space-x-2 outline-none focus:outline-none', {
            'text-secondary': !props.isActive,
            'text-white': props.isActive,
          })
        "
      >
        <div>
          <DeleteIcon />
        </div>
        <div>
          <p class="text-xs font-poppins font-light">Delete</p>
        </div>
      </button>
    </div>
    <div class="p-3.5">
      <h2 class="text-base font-poppins font-medium text-title">
        {{ props.title }}
      </h2>
      <div class="my-3">
        <p class="text-xs font-poppins font-light text-secondary">
          {{ props.desc }}
        </p>
      </div>
      <div class="flex items-center space-x-2">
        <div class="w-6 h-6 rounded-full">
          <img
            src="../../assets/avatars/male-avatar.png"
            alt=""
            class="w-full h-full object-cover rounded-full"
          />
        </div>
        <div class="w-6 h-6 rounded-full">
          <img
            src="../../assets/avatars/female-avatar.png"
            alt=""
            class="w-full h-full object-cover rounded-full"
          />
        </div>
        <div class="w-6 h-6 rounded-full">
          <img
            src="../../assets/avatars/male-avatar.png"
            alt=""
            class="w-full h-full object-cover rounded-full"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.project-row {
  border-radius: 20px;
  border: 1px solid rgba(228, 228, 228, 1);
}

.active-project-row {
  border-radius: 20px;
  border: 1px solid rgba(122, 78, 213, 1);
}
</style>
