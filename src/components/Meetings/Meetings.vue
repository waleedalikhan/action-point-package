<script setup lang="ts">
// @ts-ignore
import Card from '../global/Card.vue'
// @ts-ignore
import MeetingCard from './MeetingCard.vue'
</script>

<template>
  <div>
    <div class="w-full pt-[10px] mb-5 pl-5">
      <h2 class="text-[21px] text-title font-poppins font-bold">
        Meetings
        <span class="text-[10px] font-light text-title">
          * To see all versions of a meeting: click "Edit", then go to menu
        </span>
      </h2>
    </div>
    <div class="w-full">
      <Card>
        <MeetingCard />
        <MeetingCard />
        <MeetingCard />
      </Card>
    </div>
  </div>
</template>
