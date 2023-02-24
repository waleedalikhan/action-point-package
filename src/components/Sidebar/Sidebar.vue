<script setup lang="ts">
import { ref } from 'vue'
import cn from 'classnames'

// @ts-ignore
import SidebarBtn from './SidebarBtn.vue'
import SidebarAccountSettingsBtn from './SidebarAccountSettingsBtn.vue'

let isSidebarOpen = ref<boolean>(false)
</script>

<template>
  <div>
    <div
      class="sidebar py-[17px] min-h-[95vh] px-5 w-[266px] relative xl:block hidden"
    >
      <div class="w-full mb-[63px] flex justify-center">
        <a href="#" class="w-[52px] h-[52px]">
          <img
            src="../../assets/logo.png"
            alt=""
            class="w-full h-full object-cover"
          />
        </a>
      </div>
      <div class="w-full text-center mb-8">
        <h1 class="font-poppins text-base font-medium text-primary">
          Dashboard:
        </h1>
      </div>
      <div class="w-full flex justify-center mb-5">
        <SidebarBtn btnText="create project" />
      </div>
      <div class="w-full flex justify-center">
        <SidebarBtn btnText="add meeting" />
      </div>

      <div class="absolute bottom-5">
        <SidebarAccountSettingsBtn />
      </div>
    </div>
    <button
      class="xl:hidden w-[60px] h-[60px] bg-white rounded-full fixed left-5 top-5 z-[999999999] shadow-2xl flex items-center justify-center"
      @click="isSidebarOpen = true"
    >
      <span>
        <span class="block bg-primary w-[25px] h-[2px]"></span>
        <span class="block bg-primary w-[25px] h-[2px] my-1"></span>
        <span class="block bg-primary w-[25px] h-[2px]"></span>
      </span>
    </button>
    <div
      :class="
        cn(
          'xl:hidden block fixed z-[9999999999] inset-y-0 py-5 bg-white transition-all ease-in-out duration-300',
          {
            'left-0': isSidebarOpen,
            '-left-[300px]': !isSidebarOpen,
          },
        )
      "
    >
      <div class="sidebar py-[17px] h-full px-5 w-[266px] relative">
        <button
          class="absolute top-5 right-5 outline-none focus:outline-none"
          @click="isSidebarOpen = false"
        >
          <span
            class="block bg-primary w-[18px] h-[2px] transform rotate-[130deg] translate-x-[-2px]"
          ></span>
          <span
            class="block bg-primary w-[18px] h-[2px] transform rotate-[-130deg] translate-y-[-2px] translate-x-[-1px]"
          ></span>
        </button>

        <div class="w-full mb-[63px] flex justify-center">
          <a href="#" class="w-[52px] h-[52px]">
            <img
              src="../../assets/logo.png"
              alt=""
              class="w-full h-full object-cover"
            />
          </a>
        </div>
        <div class="w-full text-center mb-8">
          <h1 class="font-poppins text-base font-medium text-primary">
            Dashboard:
          </h1>
        </div>
        <div class="w-full flex justify-center mb-5">
          <SidebarBtn btnText="create project" />
        </div>
        <div class="w-full flex justify-center">
          <SidebarBtn btnText="add meeting" />
        </div>

        <div class="absolute bottom-5">
          <SidebarAccountSettingsBtn />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sidebar {
  border-radius: 20px;
  box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.303935);
}
</style>
