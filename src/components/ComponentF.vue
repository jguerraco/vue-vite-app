<template>
  <div class="card">
    <h2 class="callout">Component F - Conditional Rendering Example</h2>
    <button @click="toggle">Toggle Message</button>
    <p v-if="showMessage">You toggled me!</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const showMessage = ref(false)

function toggle() {
  showMessage.value = !showMessage.value
}
</script>
