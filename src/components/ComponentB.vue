<template>
  <div class="card">
    <h2 class="callout">Component B - Moment.js Example</h2>
    <p>{{ currentDate }}</p>
  </div>
</template>

<script setup>
import moment from 'moment'

const currentDate = moment().format('MMMM Do YYYY, h:mm:ss a')
</script>
