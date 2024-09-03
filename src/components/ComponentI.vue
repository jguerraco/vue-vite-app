<template>
  <div class="card">
    <h2 class="callout">Component I - Parent-Child Communication Example</h2>
    <ChildComponent @message-from-child="receiveMessage" />
    <p>{{ message }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const message = ref('')

function receiveMessage(childMessage) {
  message.value = childMessage
}
</script>
