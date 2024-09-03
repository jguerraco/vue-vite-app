<template>
  <div class="card">
    <h2 class="callout">Component A - Lodash Example</h2>
    <p>{{ reversedMessage }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import _ from 'lodash'

const message = ref('Hello Vue.js')
const reversedMessage = ref(_.reverse([...message.value]).join(''))
</script>
