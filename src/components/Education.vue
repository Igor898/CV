<template>
  <section id="education" class="section education-section">
    <div class="container">
      <h2 class="section-title">Образование</h2>
      <div class="education-cards">
        <div 
          v-for="edu in education" 
          :key="edu.institution"
          class="education-card"
        >
          <div class="education-icon">
            <i class="fas fa-graduation-cap"></i>
          </div>
          <h3 class="degree">{{ edu.degree }}</h3>
          <h4 class="institution">{{ edu.institution }}</h4>
          <span class="education-period">{{ edu.period }}</span>
          <p class="education-description">{{ edu.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const education = reactive([
  {
    degree: 'Программная инжинерия (Заочно)',
    institution: 'КубГТУ',
    period: '2022 - настоящее время',
    description: 'Специализация в области веб-технологий и человеко-компьютерного взаимодействия.'
  },
  {
    degree: 'Прикладная информатика',
    institution: 'Брюховецкий Аграрный Колледж',
    period: '2018 - 2022',
    description: 'Основное внимание уделено основам программирования, алгоритмам и структурам данных.'
  }
])
</script>