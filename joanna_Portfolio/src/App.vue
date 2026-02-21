<script setup>
import Footer from './components/Footer.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
const userName = ref('Joanna Kamikazi');
</script>
<template>
  <h1>Welcome to Kamikazi's Portfolio</h1>
  <p>Hello, {{ userName }}!</p>
  <input v-model="userName" placeholder="Enter your name" />
  <HeaderComponent />
  <Footer />
</template>