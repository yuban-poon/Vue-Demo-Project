<script setup lang="ts">
import SearchBar from '../components/SearchBar.vue'
import IconBtn from '../components/IconBtn.vue'
import Banner from '../components/Banner.vue'
import { faBell, faGear } from '@fortawesome/free-solid-svg-icons'
</script>

<template>
  <main class="flex flex-row flex-grow ml-[2rem]">
    <div class="flex flex-col flex-grow mr-[2rem]">
      <div class="flex flex-row">
        <SearchBar />
        <div class="flex flex-row w-[30%] justify-end">
          <IconBtn :icon="faBell" type="solid" class="w-[3rem]" style="color: #4264d0" />
          <IconBtn :icon="faGear" type="solid" class="ml-2 w-[3rem]" style="color: #4264d0" />
        </div>
      </div>
      <div class="flex flex-row h-[25%] mt-[2rem] w-full">
        <Banner name="Dr. Ben" day="Monday" />
      </div>
    </div>
    <div class="w-1/3 flex flex-col">
      <div class="flex flex-row">
        <SearchBar />
      </div>
    </div>
  </main>
</template>
