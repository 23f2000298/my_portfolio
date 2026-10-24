<script setup>
import profile from '../data/profile.json'
</script>

<template>
  <section id="home" class="hero" aria-labelledby="hero-title">
    <div class="container hero__inner">
      <h1 id="hero-title" class="hero__name">{{ profile.name }}</h1>
      <p class="hero__headline">{{ profile.headline }}</p>
      <p class="hero__intro">{{ profile.intro }}</p>
      <div class="hero__actions">
        <a class="btn btn--primary" href="#projects">View My Projects</a>
        <a class="btn btn--secondary" href="#contact">Contact Me</a>
      </div>
    </div>
  </section>
</template>
