<script setup>
import Footer from './components/Footer.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
const userName = ref('Joanna Kamikazi');
import {ref} from 'vue';
const show = ref(true);
</script>
<template>
  <h1>Welcome to Kamikazi's Portfolio</h1>
  <p>Hello, {{ userName }}!</p>
  <input v-model="userName" placeholder="Enter your name" />
  <HeaderComponent />
  <Footer />
  <button @click="show = !show">Toggle</button>
  <p v-if="show">Visible using v-if!</p>
  <p v-show="show">Visible using v-show</p>
</template>