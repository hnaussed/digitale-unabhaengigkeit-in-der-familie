<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

const { currentPage, total } = useNav()
const pageNumber = computed(() => currentPage.value)
</script>

<template>
  <footer class="slide-footer">
    <span>DiDay Darmstadt: Digitale Unabhängigkeit in der Familie</span>
    <span>{{ pageNumber }} / {{ total }}</span>
  </footer>
</template>

<style scoped>
.slide-footer {
  position: absolute;
  right: 1.5rem;
  bottom: 0.75rem;
  left: 1.5rem;
  display: flex;
  justify-content: space-between;
  color: #64748b;
  font-size: 0.65rem;
}
</style>