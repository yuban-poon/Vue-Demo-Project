<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faSearch } from '@fortawesome/free-solid-svg-icons'
</script>

<template>
  <div id="searchbar" class="p-3 flex items-center flex-grow bg-white rounded-xl">
    <input
      type="text"
      class="flex-grow focus:outline-none"
      placeholder="Search for events, patients etc."
    />
    <FontAwesomeIcon id="searchicon" :icon="faSearch" size="lg" />
  </div>
</template>

<style scoped>
#searchicon {
  color: #4264d0;
}
</style>
