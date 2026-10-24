<script setup>
import SectionWrapper from './SectionWrapper.vue'
import skills from '../data/skills.json'
</script>

<template>
  <SectionWrapper id="skills" title="Skills" intro="The tools I use most for data analysis and machine learning.">
    <div class="grid grid--skills">
      <article v-for="group in skills" :key="group.title" class="card">
        <h3 class="card__title">{{ group.title }}</h3>
        <ul class="tags">
          <li v-for="item in group.items" :key="item">{{ item }}</li>
        </ul>
      </article>
    </div>
  </SectionWrapper>
</template>
