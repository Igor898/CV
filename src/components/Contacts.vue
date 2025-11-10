<template>
  <section id="contacts" class="section contacts-section">
    <div class="container">
      <h2 class="section-title">Контакты</h2>
      <div class="contacts-content">
        <div class="contact-info">
          <div 
            v-for="contact in contacts" 
            :key="contact.type"
            class="contact-item"
          >
            <div class="contact-icon">
              <img class="contact-img" :src="contact.icon">
            </div>
            <div class="contact-details">
              <h3>{{ contact.type }}</h3>
              <a 
                :href="contact.link" 
                :target="contact.external ? '_blank' : '_self'"
              >
                {{ contact.value }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'
import emailIcon from '../assets/images/email.png';
import phoneIcon from '../assets/images/phone-call.png';
import githubIcon from '../assets/images/github.png';
import telegramIcon from '../assets/images/paper-plane.png';

const contacts = reactive([
  {
    type: 'Email',
    value: 'potemkin_2002@bk.ru',
    icon: emailIcon,
    link: 'mailto:potemkin_2002@bk.ru'
  },
  {
    type: 'Телефон',
    value: '+7 (961) 510-69-81',
    icon: phoneIcon,
    link: 'tel:+79615106981'
  },
  {
    type: 'GitHub',
    value: 'github.com/Igor898',
    icon: githubIcon,
    link: 'https://github.com/Igor898',
    external: true
  },
  {
    type: 'Telegram',
    value: 'https://t.me/iona_dev',
    icon: telegramIcon,
    link: 'https://t.me/iona_dev',
    external: true
  }
])
</script>
