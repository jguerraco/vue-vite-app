<template>
  <div class="card">
    <h2 class="callout">Component G - List Rendering Example</h2>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script setup>
const items = ['Item 1', 'Item 2', 'Item 3', 'Item 4']
</script>
