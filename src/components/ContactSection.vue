<script setup>
import SectionWrapper from './SectionWrapper.vue'
import contact from '../data/contact.json'

const gmailLink = `https://mail.google.com/mail/?view=cm&to=${contact.email}`
const linkedinLabel = contact.linkedin.replace('https://www.', '')
const githubLabel = contact.github.replace('https://', '')
const kaggleLabel = contact.kaggle.replace('https://www.', '')
</script>

<template>
  <SectionWrapper
    id="contact"
    title="Contact"
    intro="I am open to internships and entry-level roles in data analysis, data science and machine learning. Send me a message and I will reply as soon as I can."
    alt
  >
    <ul class="contact">
      <li>
        <span class="contact__label">Email</span>
        <a :href="gmailLink" target="_blank" rel="noopener noreferrer">{{ contact.email }}</a>
      </li>
      <li>
        <span class="contact__label">LinkedIn</span>
        <a :href="contact.linkedin" target="_blank" rel="noopener noreferrer">{{ linkedinLabel }}</a>
      </li>
      <li>
        <span class="contact__label">GitHub</span>
        <a :href="contact.github" target="_blank" rel="noopener noreferrer">{{ githubLabel }}</a>
      </li>
      <li>
        <span class="contact__label">Kaggle</span>
        <a :href="contact.kaggle" target="_blank" rel="noopener noreferrer">{{ kaggleLabel }}</a>
      </li>
    </ul>
    <a class="btn btn--primary" :href="gmailLink" target="_blank" rel="noopener noreferrer">Send an email</a>
  </SectionWrapper>
</template>