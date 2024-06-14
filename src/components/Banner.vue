<script setup lang="ts">
import Date from './Date.vue'
defineProps<{ name: string; day: string }>()
</script>

<template>
  <div class="rounded-xl px-4 h-full w-full flex flex-row text-white" style="background-color: #4264d0">
    <div class="flex flex-col h-full py-4 flex-grow ">
      <Date />
      <div class="flex flex-grow flex-col justify-end">
        <span class="font-bold text-3xl">Good Day, {{ name }}!</span>
        <span>Have a Nice {{ day }}!</span>
      </div>
    </div>
    <img class="h-full content-end items-end" src="../assets/images/Dr.png" alt="">
  </div>
</template>
