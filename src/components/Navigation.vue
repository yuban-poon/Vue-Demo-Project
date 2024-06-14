<script setup lang="ts">
defineProps<{
  name: string
}>()
import { RouterLink, RouterView } from 'vue-router'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import {
  faHouse,
  faUser,
  faCalendarDays,
  faLayerGroup,
  faArrowRightFromBracket
} from '@fortawesome/free-solid-svg-icons'
import { ref } from 'vue'
const rlStyle = ref(
  'w-10 h-10 mb-10 content-center hover:bg-opacity-50 hover:bg-gray-300 hover:rounded-lg'
)
</script>

<template>
  <header
    id="navigator"
    class="p-4 rounded-2xl content-center text-white h-[calc(100vh-4rem)] flex flex-col"
  >
    <span class="text-center text-xl font-bold">{{ name }} </span>
    <nav class="flex-grow mx-auto py-4 mt-8 flex flex-col text-center">
      <RouterLink :class="rlStyle" to="/">
        <FontAwesomeIcon size="xl" class="m-auto" :icon="faHouse" />
      </RouterLink>
      <RouterLink :class="rlStyle" to="/about">
        <FontAwesomeIcon size="xl" class="m-auto" :icon="faUser" />
      </RouterLink>
      <RouterLink :class="rlStyle" to="/">
        <FontAwesomeIcon size="xl" class="m-auto" :icon="faCalendarDays" />
      </RouterLink>
      <RouterLink :class="rlStyle" to="/about">
        <FontAwesomeIcon size="xl" class="m-auto" :icon="faLayerGroup" />
      </RouterLink>
      <RouterLink class="flex-grow content-end" to="/about">
        <div :class="rlStyle" class="mb-0">
          <FontAwesomeIcon size="xl" class="m-auto" :icon="faArrowRightFromBracket" />
        </div>
      </RouterLink>
    </nav>
  </header>
</template>

<style scoped>
#navigator {
  background-color: #4264d0;
  width: 6rem;
}
</style>
