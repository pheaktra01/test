<script setup lang="ts">
const { title, description, tech, link } = defineProps<{
  title: string
  description: string
  tech?: string
  link?: string
}>()
</script>

<template>
  <article class="card">
      <header class="card-header">
      <h3>{{ title }}</h3>
    </header>
    <p class="card-desc">{{ description }}</p>
    <p class="card-tech" v-if="tech">Tech: {{ tech }}</p>
    <div class="card-actions">
      <a v-if="link" :href="link" target="_blank" rel="noopener" class="btn">View</a>
    </div>
  </article>
</template>

<style scoped>
.card {
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  padding: 16px;
  background: #fff;
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.card-header h3 { margin: 0; font-size: 1.05rem; }
.card-desc { color: #374151; margin: 0; flex: 1; }
.card-tech { font-size: 0.85rem; color: #6b7280; margin: 0; }
.card-actions { display:flex; justify-content:flex-end; }
.btn { background:#111827; color:#fff; padding:6px 10px; border-radius:6px; text-decoration:none; font-size:0.9rem; }
</style>
