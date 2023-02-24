<script setup lang="ts">
import CalendarIcon from '../global/icons/CalendarIcon.vue'
import ClockIcon from '../global/icons/ClockIcon.vue'
import DeleteIcon from '../global/icons/DeleteIcon.vue'
import PencilIcon from '../global/icons/PencilIcon.vue'
</script>

<template>
  <div class="p-5 rounded-[20px] border border-[#e4e4e4] mb-5">
    <div class="flex items-center space-x-2">
      <div class="flex space-x-2 items-center text-title">
        <div>
          <CalendarIcon />
        </div>
        <div>
          <p class="text-xs font-light text-title">23.01.23</p>
        </div>
      </div>
      <div class="flex space-x-2 items-center text-title">
        <div>
          <ClockIcon />
        </div>
        <div>
          <p class="text-xs font-light text-title">04.02 PM</p>
        </div>
      </div>
      <div class="flex space-x-2 items-center text-title">
        <div>
          <ClockIcon />
        </div>
        <div>
          <p class="text-xs font-light text-title">19 min.</p>
        </div>
      </div>
    </div>
    <div class="my-5">
      <h2 class="text-base font-poppins font-medium text-title">
        Meeting subject bla bla
      </h2>
    </div>
    <div class="flex item-start space-x-3">
      <div>
        <h2 class="text-base font-poppins font-medium text-title">Keywords:</h2>
      </div>
      <div class="flex flex-wrap gap-3">
        <div class="px-6 pb-1 bg-light border border-[#e4e4e4] rounded-[20px]">
          <span class="text-xs font-light font-open-sans text-title">
            bla bla
          </span>
        </div>
        <div class="px-6 pb-1 bg-light border border-[#e4e4e4] rounded-[20px]">
          <span class="text-xs font-light font-open-sans text-title">
            bla bla
          </span>
        </div>
        <div class="px-6 pb-1 bg-light border border-[#e4e4e4] rounded-[20px]">
          <span class="text-xs font-light font-open-sans text-title">
            bla bla
          </span>
        </div>
        <div class="px-6 pb-1 bg-light border border-[#e4e4e4] rounded-[20px]">
          <span class="text-xs font-light font-open-sans text-title">
            bla bla
          </span>
        </div>
        <div class="px-6 pb-1 bg-light border border-[#e4e4e4] rounded-[20px]">
          <span class="text-xs font-light font-open-sans text-title">
            bla bla
          </span>
        </div>
        <div class="px-6 pb-1 bg-light border border-[#e4e4e4] rounded-[20px]">
          <span class="text-xs font-light font-open-sans text-title">
            bla bla
          </span>
        </div>
      </div>
    </div>
    <div class="my-5 flex items-center space-x-4">
      <div>
        <p class="text-base font-poppins font-medium text-title">Attendees:</p>
      </div>
      <div class="flex space-x-2">
        <div>
          <div class="w-6 h-6 rounded-full">
            <img
              src="../../assets/avatars/female-avatar.png"
              alt=""
              class="w-full h-full object-cover rounded-full"
            />
          </div>
        </div>
        <div>
          <div class="w-6 h-6 rounded-full">
            <img
              src="../../assets/avatars/male-avatar.png"
              alt=""
              class="w-full h-full object-cover rounded-full"
            />
          </div>
        </div>
        <div>
          <div class="w-6 h-6 rounded-full">
            <img
              src="../../assets/avatars/female-avatar.png"
              alt=""
              class="w-full h-full object-cover rounded-full"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="flex justify-end space-x-4">
      <div>
        <button
          class="w-[85px] flex items-center justify-center bg-primary text-white py-1 outline-none focus:outline-none rounded-[20px]"
        >
          <div class="flex space-x-2">
            <span>
              <PencilIcon />
            </span>
            <span class="text-white text-xs font-poppins font-light">Edit</span>
          </div>
        </button>
      </div>
      <div>
        <button
          class="w-[100px] flex items-center justify-center bg-title text-white py-1 outline-none focus:outline-none rounded-[20px]"
        >
          <div class="flex space-x-2">
            <span>
              <DeleteIcon />
            </span>
            <span class="text-white text-xs font-poppins font-light">
              Delete
            </span>
          </div>
        </button>
      </div>
    </div>
  </div>
</template>
