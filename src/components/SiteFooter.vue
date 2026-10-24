<script setup>
import profile from '../data/profile.json'

const year = new Date().getFullYear()
</script>

<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; {{ year }} {{ profile.name }}. Built with Vue and Vite.</p>
    </div>
  </footer>
</template>
