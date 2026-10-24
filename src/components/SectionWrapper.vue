<script setup>
defineProps({
  id: { type: String, required: true },
  title: { type: String, required: true },
  intro: { type: String, default: '' },
  alt: { type: Boolean, default: false },
})
</script>

<template>
  <section :id="id" :class="['section', { 'section--alt': alt }]" :aria-labelledby="`${id}-title`">
    <div class="container">
      <h2 :id="`${id}-title`" class="section__title">{{ title }}</h2>
      <p v-if="intro" class="section__intro">{{ intro }}</p>
      <slot />
    </div>
  </section>
</template>
