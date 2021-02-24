<template>
  <Navbar />
  <div class="view">
    <router-view />
  </div>
  <Footer />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Navbar from '@/components/Navbar.vue'; // @ is an alias to /src
import Footer from '@/components/Footer.vue';

@Options({
  components: {
    Navbar,
    Footer,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Asap:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Sacramento&display=swap');

body {
  background-color: black;
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fff;
  padding: 16px 48px 16px 48px;
  @media (max-width: 768px) {
    padding: 8px 0 0 0;
  }
}

h1 {
  font-family: 'Asap', sans-serif;
  letter-spacing: 1px;
}

h1::first-letter {
  font-size: 48px;
  font-family: 'Sacramento', cursive;
  color: #be2623;
}

h2 {
  font-family: 'Poppins', sans-serif;
  font-size: 32px;
}

.view {
  text-align: center;
}

a {
  color: white;
  text-decoration: none;
}

a:hover {
  border-style: solid;
  border-width: 0 0 1px 0;
  border-color: #be2623;
  animation: borderFadeInAnimation ease 0.5s;
}

@keyframes borderFadeInAnimation {
  0% {
    border-color: black;
  }
  100% {
    border-color: #be2623;
  }
}
</style>
