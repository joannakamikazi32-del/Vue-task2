<script setup>
import Footer from './components/Footer.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
const userName = ref('Joanna Kamikazi');
const show = ref(true);
const count = ref(0);
function increase() {
  count.value++;
};
import MessageComponent from './components/MessageComponent.vue';
  import { onMounted } from 'vue';
onMounted(() => {
  console.log('Component has been mounted!');
});
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
  <p>count:{{ count }}</p>
  <button @click="increase">increase</button>
<nav>
  <router-link to="/">Home</router-link>
  <router-link to="/about">About</router-link>
</nav>
<router-view></router-view>
<MessageComponent message="This is a message from the parent component!" />
</template>