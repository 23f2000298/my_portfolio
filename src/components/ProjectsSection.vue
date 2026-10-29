<script setup>
import SectionWrapper from './SectionWrapper.vue'
import ProjectCard from './ProjectCard.vue'
import projects from '../data/projects.json'
import contact from '../data/contact.json'
</script>

<template>
  <SectionWrapper
    id="projects"
    title="Projects"
    intro="Selected projects I have built during my studies."
    alt
  >
    <div class="grid grid--projects">
      <ProjectCard v-for="p in projects" :key="p.title" :project="p" />
    </div>

    <div class="projects__more">
      <p>Please visit my GitHub and Kaggle to see all my projects.</p>
      <div class="projects__more-actions">
        <a class="btn btn--secondary" :href="contact.github" target="_blank" rel="noopener noreferrer">
          Visit my GitHub
        </a>
        <a class="btn btn--primary" :href="contact.kaggle" target="_blank" rel="noopener noreferrer">
          Visit my Kaggle
        </a>
      </div>
    </div>
  </SectionWrapper>
</template>