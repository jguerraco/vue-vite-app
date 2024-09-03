<template>
  <div class="card">
    <h2 class="callout">Component C - Axios Example</h2>
    <ul>
      <li v-for="(post, index) in posts" :key="index">{{ post.title }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

const posts = ref([])

onMounted(async () => {
  try {
    const response = await axios.get('https://jsonplaceholder.typicode.com/posts')
    posts.value = response.data.slice(0, 5) // Only display the first 5 posts
  } catch (error) {
    console.error(error)
  }
})
</script>
