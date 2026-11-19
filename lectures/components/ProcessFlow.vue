<script setup lang="ts">
defineProps<{
  steps: { title: string; detail: string }[]
}>()
</script>

<template>
  <ol class="process-flow" aria-label="단계별 작업 순서">
    <li v-for="step in steps" :key="step.title">
      <h2>{{ step.title }}</h2>
      <p>{{ step.detail }}</p>
    </li>
  </ol>
</template>

<style scoped>
.process-flow {
  display: grid;
  grid-auto-columns: minmax(0, 1fr);
  grid-auto-flow: column;
  gap: 2.75rem;
  margin: 2rem 0 1.65rem;
  padding: 0;
  list-style: none;
}

.process-flow li {
  position: relative;
  margin: 0;
  padding: 0.9rem 0 0;
  border-top: 1px solid var(--hairline);
}

.process-flow li + li::before {
  position: absolute;
  top: 1.35rem;
  left: -1.65rem;
  width: 0.55rem;
  height: 0.55rem;
  border-top: 2px solid var(--slidev-theme-primary);
  border-right: 2px solid var(--slidev-theme-primary);
  content: '';
  transform: rotate(45deg);
}

.process-flow h2 {
  margin: 0 0 0.4rem;
  font-size: 1.24rem;
  line-height: 1.4;
}

.process-flow p {
  margin: 0;
  line-height: 1.6;
}
</style>
