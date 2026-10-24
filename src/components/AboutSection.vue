<script setup>
import SectionWrapper from './SectionWrapper.vue'
import profile from '../data/profile.json'
</script>

<template>
  <SectionWrapper id="about" title="About me" alt>
    <div class="about">
      <div class="about__text">
        <p v-for="paragraph in profile.about" :key="paragraph">{{ paragraph }}</p>
      </div>
      <dl class="facts">
        <div><dt>Studying</dt><dd>BS in Data Science and Applications, IIT Madras</dd></div>
        <div><dt>Goal</dt><dd>Data Analyst, Data Scientist or ML Engineer</dd></div>
        <div><dt>Location</dt><dd>{{ profile.location }}</dd></div>
      </dl>
    </div>
  </SectionWrapper>
</template>
