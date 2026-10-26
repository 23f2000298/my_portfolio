<script setup>
import SectionWrapper from './SectionWrapper.vue'
import ProjectCard from './ProjectCard.vue'
import projects from '../data/projects.json'
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
  </SectionWrapper>
</template>
