<script setup>
defineProps({
  project: { type: Object, required: true },
})
</script>

<template>
  <article class="card card--project">
    <h3 class="card__title">{{ project.title }}</h3>
    <p class="card__text">{{ project.description }}</p>
    <ul class="tags" aria-label="Technologies used">
      <li v-for="t in project.tech" :key="t">{{ t }}</li>
    </ul>
    <div class="card__actions">
      <a class="btn btn--small btn--secondary" :href="project.github" target="_blank" rel="noopener noreferrer">
        GitHub<span class="visually-hidden"> repository for {{ project.title }}</span>
      </a>
      <a class="btn btn--small btn--primary" :href="project.demo" target="_blank" rel="noopener noreferrer">
        Live demo<span class="visually-hidden"> of {{ project.title }}</span>
      </a>
    </div>
  </article>
</template>
