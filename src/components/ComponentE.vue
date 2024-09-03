<template>
  <div class="card">
    <h2 class="callout">Component E - Reactive Input Example</h2>
    <input v-model="name" placeholder="Enter your name" />
    <p>Hello, {{ name }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
</script>
