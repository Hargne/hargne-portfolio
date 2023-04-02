<script setup lang="ts">
defineProps<{
  title?: string
  background?: 'circles' | 'dark'
  fullHeight?: boolean
}>()
</script>

<template>
  <section :class="[background, fullHeight && 'full-height']">
    <div class="content">
      <h2 v-if="title">{{ title }}</h2>
      <slot></slot>
    </div>
  </section>
</template>

<style scoped>
h2 {
  font-size: 2rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 3rem;
  text-transform: uppercase;
}

section {
  padding: 4rem 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
  background-color: var(--secondary-bg-color);
}

.content {
  max-width: 30rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.circles {
  background-color: #264653;
  background-image: repeating-radial-gradient(circle at 0 0, transparent 0, #264653 40px),
    repeating-linear-gradient(#1c333c, #1c333c);
}

.dark {
  background-color: var(--dark-background-color);
  color: var(--primary-color);
  fill: var(--primary-color);
}

.full-height {
  min-height: 100vh;
}
</style>
