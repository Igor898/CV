<template>
  <section id="experience" class="section experience-section">
    <div class="container">
      <h2 class="section-title">Опыт работы</h2>
      <div class="timeline">
        <div 
          v-for="(job, index) in workExperience" 
          :key="job.company"
          class="timeline-item"
          :class="{ 'timeline-item-right': index % 2 === 0 }"
        >
          <div class="timeline-marker"></div>
          <div class="timeline-content">
            <h3 class="job-title">{{ job.position }}</h3>
            <h4 class="company">{{ job.company }}</h4>
            <span class="period">{{ job.period }}</span>
            <p class="job-description">{{ job.description }}</p>
            <div class="job-tech">
              <span 
                v-for="tech in job.technologies" 
                :key="tech"
                class="tech-tag"
              >
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const workExperience = reactive([
  {
    position: 'Frontend Developer',
    company: 'Фриланс проект',
    period: 'Август 2025 - Сентябрь 2025',
    description: 'Разработка фронтенд части для приложения переименовыванию файлов на Vue3.',
    technologies: ['Vue.js', 'TypeScript', 'Sass', 'Vite']
  },
  {
    position: 'Frontend Developer',
    company: 'Digital Agency',
    period: 'Апрель 2025 - Май 2025',
    description: 'Создание Telegram mini app приложение интернет магазина на React + TS',
    technologies: ['React', 'TypeScript', 'Sass', 'Vite']
  },
  {
    position: 'Junior Frontend Developer',
    company: 'AXAS',
    period: 'Ноябрь 2024 - Декабрь 2024',
    description: 'Разработка пользовательских интерфейсов и участие в создании MVP для стартапов.',
    technologies: ['Vue.js', 'TypeScript', 'Sass', 'Vite']
  }
])
</script>