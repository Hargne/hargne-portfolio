<script setup lang="ts">
export interface WorkEntry {
  title: string
  year: number
  type: 'game' | 'motion-picture'
  url?: string
}

defineProps<WorkEntry>()
</script>

<template>
  <a :href="url" class="container" target="_blank">
    <span class="title">{{ title }}</span>
    <span class="year">({{ year }})</span>
  </a>
</template>

<style scoped>
.container {
  display: flex;
  align-items: center;
  color: var(--text-color);
  text-decoration: none;
  transition: all 0.2s;
}
.title {
  background-color: var(--text-color);
  color: var(--primary-color);
  font-weight: 700;
  padding: 1rem;
  transition: all 0.3s;
}
.container:hover {
  transform: translateX(1.5rem) scale(1.2);
}
.container:hover .title {
  color: #fff;
}
.year {
  padding: 1rem;
  font-weight: 300;
}
</style>
