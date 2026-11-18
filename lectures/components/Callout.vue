<script setup lang="ts">
// 강조 블록. 본문 슬롯에 내용을 넣고, title 로 짧은 머리말을 붙일 수 있다.
//   <Callout title="핵심">분모가 다르면 같은 퍼널 단계가 아니다.</Callout>
defineProps<{
  title?: string
}>()
</script>

<template>
  <div class="callout">
    <div v-if="title" class="callout-title">{{ title }}</div>
    <div class="callout-body"><slot /></div>
  </div>
</template>

<style scoped>
.callout {
  font-family: var(--font-code);
  background: var(--wash);
  border-left: 3px solid var(--slidev-theme-primary);
  border-radius: 0 12px 12px 0;
  padding: 0.9rem 1.4rem;
  margin: 1.25rem 0;
  line-height: 1.7;
}
.callout-title {
  font-weight: 700;
  font-size: 0.8em;
  letter-spacing: 0.06em;
  color: var(--slidev-theme-primary);
  margin-bottom: 0.25rem;
}
.callout-body :deep(p) {
  margin: 0;
}
</style>
