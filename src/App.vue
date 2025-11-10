<template>
  <div id="app">
    <Header />
    <main class="main-content">
      <AboutMe />
      <Skills />
      <WorkExperience />
      <Education />
      <Contacts />
    </main>
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import AboutMe from './components/AboutMe.vue'
import Skills from './components/Skills.vue'
import WorkExperience from './components/WorkExperience.vue'
import Education from './components/Education.vue'
import Contacts from './components/Contacts.vue'
</script>