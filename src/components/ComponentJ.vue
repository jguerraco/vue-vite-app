<template>
  <div class="card">
    <h2 class="callout">Component J - Lifecycle Hooks Example</h2>
    <p>Component has been mounted {{ timesMounted }} times.</p>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const timesMounted = ref(0)

onMounted(() => {
  timesMounted.value += 1
})
</script>
