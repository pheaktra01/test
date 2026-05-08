<script setup lang="ts">
import Portfolio from './components/Portfolio.vue'
</script>

<template>
  <div id="app">
    <header style="padding:18px; text-align:center; background:linear-gradient(90deg,#f3f4f6,#fff)">
      <h2>My Vue Portfolio</h2>
      <p style="margin:6px 0; color:#6b7280">A collection of projects from this course.</p>
    </header>

    <main>
      <Portfolio />
    </main>
  </div>
</template>

<style scoped>
#app { font-family: Inter, ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; color:#111827; }
main { padding-bottom: 40px; }
</style>
