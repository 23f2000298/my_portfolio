<script setup>
import { ref } from 'vue'
import profile from '../data/profile.json'

const open = ref(false)
const close = () => { open.value = false }
</script>

<template>
  <header class="navbar">
    <div class="container navbar__inner">
      <a href="#home" class="navbar__brand" @click="close">{{ profile.name }}</a>
      <button
        class="navbar__toggle"
        :aria-expanded="open"
        aria-controls="primary-nav"
        @click="open = !open"
      >
        {{ open ? 'Close' : 'Menu' }}
      </button>
      <nav id="primary-nav" aria-label="Primary" :class="['navbar__links', { 'is-open': open }]">
        <ul>
          <li v-for="item in profile.nav" :key="item.id">
            <a :href="`#${item.id}`" @click="close">{{ item.label }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
