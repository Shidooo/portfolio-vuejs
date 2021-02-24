<template>
  <div class="projects">
    <Card
      title="Portfolio-vuejs"
      description="My portfolio"
      github="https://github.com/shidooo/Portfolio-vuejs"
    />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Card from '@/components/Card.vue'; // @ is an alias to /src

@Options({
  components: {
    Card,
  },
})
export default class Projects extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.h2 {
  margin-bottom: 48px;
}

.projects {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.card {
  animation: fadeInAnimation ease 2s;
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
