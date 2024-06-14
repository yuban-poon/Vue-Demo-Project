<script setup lang="ts">
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
defineProps<{ icon: Object }>()
function search() {
  console.log('searching...')
}
</script>

<template>
  <div id="box" class="flex bg-white rounded-xl" @click="search">
    <FontAwesomeIcon size="lg" class="m-auto" :icon="icon" />
  </div>
</template>

<style scoped></style>
