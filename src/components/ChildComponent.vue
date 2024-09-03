<template>
  <div>
    <button @click="sendMessage">Send Message to Parent</button>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue'

const emit = defineEmits(['message-from-child'])

function sendMessage() {
  emit('message-from-child', 'Hello from Child')
}
</script>
