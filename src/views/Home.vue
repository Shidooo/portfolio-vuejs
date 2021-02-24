<template>
  <img class="avatar" src="avatar.png" />
  <br />
  <p class="quote">
    <q>Elegance transcends time</q>
  </p>
  <h2>I AM FULLSTACK WEB DEVELOPER</h2>
  <p class="article">
    My name is Julien, I am 22 years old, I am from Switzerland.
    I am a student in computer science, motivated by entrepreneurship.
    I like to build projects and see them grow.
  </p>
  <br />
  <img class="calendar" src="https://ghchart.rshah.org/be2623/Shidooo" alt="Shidooo's Github chart" />
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';

export default class Home extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.quote {
  margin-bottom: 48px;
  animation: fadeInAnimation ease 1s;
}

.article {
  display: inline-block;
  width: 100%;
  max-width: 500px;
  animation: fadeInAnimation ease 3s;
  @media (max-width: 768px) {
    max-width: none;
  }
}

.avatar {
  width: 125px;
  height: 125px;
  border-radius: 50%;
  border-style: solid;
  border-color: #be2623;
  border-width: 2px;
  margin-top: 48px;
  animation: fadeInAnimation ease 1s;
  @media (max-width: 768px) {
    width: 100px;
    height: 100px;
  }
}

.calendar {
  margin-top: 48px;
  animation: fadeInAnimation ease 4s;
  @media (max-width: 768px) {
    display: none;
  }
}

@keyframes fadeInAnimation {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
