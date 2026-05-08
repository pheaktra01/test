<script setup lang="ts">
import { reactive } from 'vue'
import ProjectCard from './ProjectCard.vue'

const projects = reactive([
  {
    id: 1,
    title: 'Personal Website',
    description: 'A personal website built with Vue 3 and Vite to showcase projects and blog posts.',
    tech: 'Vue 3, Vite, TypeScript',
    link: '#'
  },
  {
    id: 2,
    title: 'Todo App',
    description: 'Simple todo app demonstrating components, localStorage persistence and composition API.',
    tech: 'Vue 3, Pinia (planned)',
    link: '#'
  },
  {
    id: 3,
    title: 'Photo Gallery',
    description: 'Responsive gallery with lazy-loaded images and CSS grid layout.',
    tech: 'Vue 3, CSS Grid',
    link: '#'
  }
])
</script>

<template>
  <section class="portfolio">
    <div class="intro">
      <h1>Portfolio</h1>
      <p>Selected projects from this course and personal experiments.</p>
    </div>

    <div class="grid">
      <ProjectCard
        v-for="p in projects"
        :key="p.id"
        :title="p.title"
        :description="p.description"
        :tech="p.tech"
        :link="p.link"
      />
    </div>
  </section>
</template>

<style scoped>
.portfolio { max-width: 960px; margin: 24px auto; padding: 0 16px; }
.intro h1 { margin: 0 0 8px 0; }
.intro p { margin: 0 0 18px 0; color: #6b7280; }
.grid { display:grid; grid-template-columns: repeat(1,1fr); gap: 12px; }
@media(min-width:600px){ .grid{ grid-template-columns: repeat(2,1fr); } }
@media(min-width:900px){ .grid{ grid-template-columns: repeat(3,1fr); } }
</style>
