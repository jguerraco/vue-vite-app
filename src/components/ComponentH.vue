<template>
  <div class="card">
    <h2 class="callout">Component H - Computed Property Example</h2>
    <input v-model="num" type="number" />
    <p>Square of {{ num }} is {{ square }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const num = ref(0)
const square = computed(() => num.value * num.value)
</script>
