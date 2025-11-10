<template>
  <section id="about" class="section about-section">
    <div class="container">
      <h2 class="section-title">Обо мне</h2>
      <div class="about-content">
        <div class="about-text">
          <p>{{ aboutData.description1 }}</p>
        </div>
        <div class="about-visual">
          <div class="code-animation">
            <div 
              v-for="(line, index) in codeLines" 
              :key="index"
              class="code-line"
              :style="{ width: line.width, animationDelay: line.delay }"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const aboutData = reactive({
  description1: 'Приветствую! Меня зовут Игорь, я frontend-разработчик с опытом работы в студии мобильной разработке AXAS, где разрабатывал кастомные веб-приложения на Vue.js. Люблю создавать удобные, быстрые и эстетичные интерфейсы, разбираться в сложных задачах и постоянно прокачивать свои навыки. Люблю фронтенд, хочу в нем развиваться и быть полезным для решения различных бизнес задач.',
})

const codeLines = reactive([
  { width: '100px', delay: '0s' },
  { width: '150px', delay: '0.5s' },
  { width: '80px', delay: '1s' }
])
</script>