<script setup lang="ts">
import type { WorkEntry } from './HomeWorkListEntry.vue'
import HomeWorkListEntry from './HomeWorkListEntry.vue'

defineProps<{
  entries: WorkEntry[]
}>()
</script>

<template>
  <ul>
    <li v-for="entry in entries" :key="entry.title">
      <HomeWorkListEntry v-bind="entry" />
    </li>
  </ul>
</template>

<style scoped>
ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

li {
  margin-bottom: 1rem;
}
</style>
