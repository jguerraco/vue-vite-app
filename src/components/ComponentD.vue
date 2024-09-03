<template>
  <div class="card">
    <h2 class="callout">Component D - D3.js Example</h2>
    <div ref="chart"></div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import * as d3 from 'd3'

const chart = ref(null)

onMounted(() => {
  const data = [30, 80, 45, 60, 20, 90, 50]

  const svg = d3.select(chart.value)
    .append('svg')
    .attr('width', 300)
    .attr('height', 150)

  svg.selectAll('rect')
    .data(data)
    .enter()
    .append('rect')
    .attr('x', (d, i) => i * 35)
    .attr('y', d => 150 - d)
    .attr('width', 30)
    .attr('height', d => d)
    .attr('fill', 'teal')
})
</script>

<style scoped>
svg {
  background-color: #f0f0f0;
}
</style>
