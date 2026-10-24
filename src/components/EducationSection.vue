<script setup>
import SectionWrapper from './SectionWrapper.vue'
import education from '../data/education.json'
</script>

<template>
  <SectionWrapper id="education" title="Education">
    <ol class="timeline">
      <li v-for="e in education" :key="e.degree" class="timeline__item">
        <h3 class="card__title">{{ e.degree }}</h3>
        <p class="timeline__school">{{ e.school }}</p>
        <p class="timeline__status">{{ e.status }}</p>
      </li>
    </ol>
  </SectionWrapper>
</template>
