<template>
  <section id="skills" class="section skills-section">
    <div class="container">
      <h2 class="section-title">Навыки</h2>
      <div class="skills-grid">
        <div 
          v-for="(skill, index) in skills" 
          :key="skill.name"
          class="skill-card"
          :style="{ animationDelay: `${index * 0.1}s` }"
        >
          <div class="skill-icon">
            <i :class="skill.icon"></i>
          </div>
          <h3 class="skill-name">{{ skill.name }}</h3>
          <div class="skill-level">
            <div 
              class="skill-progress" 
              :style="{ width: skill.level }"
            ></div>
          </div>
          <span class="skill-percentage">{{ skill.level }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const skills = reactive([
  { name: 'Vue.js', level: '90%', icon: 'fab fa-vuejs' },
  { name: 'JavaScript', level: '80%', icon: 'fab fa-js' },
  { name: 'HTML/CSS', level: '98%', icon: 'fab fa-html5' },
  { name: 'Sass/SCSS', level: '85%', icon: 'fab fa-sass' },
  { name: 'React', level: '50%', icon: 'fab fa-react' },
  { name: 'TypeScript', level: '75%', icon: 'fas fa-code' },
  { name: 'Git', level: '88%', icon: 'fab fa-git' },
  { name: 'Vite', level: '70%', icon: 'fas fa-cube' },
  { name: 'REST API', level: '100%', icon: 'fab fa-vuejs' },
  { name: 'vuetify', level: '75%', icon: 'fab fa-js' },
  { name: 'Nuxt', level: '50%', icon: 'fab fa-html5' },
  { name: 'Axios', level: '100%', icon: 'fab fa-sass' },
  { name: 'Pinia', level: '80%', icon: 'fab fa-react' },
  { name: 'WebSocket', level: '75%', icon: 'fas fa-code' },
  { name: 'Composition API', level: '100%', icon: 'fab fa-git' },
  { name: 'Node.js', level: '70%', icon: 'fas fa-cube' }
])
</script>