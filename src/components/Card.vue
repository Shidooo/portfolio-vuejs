<template>
  <div class="card">
    <h2>
      <a v-bind:href="github" target="_blank">{{title}}</a>
    </h2>
    <p>{{description}}</p>
    <a class="icon" v-bind:href="github" target="_blank">
      <img width="16" src="github.png" />
    </a>
    <a class="icon" v-bind:href="web" target="_blank">
      <img width="16" src="web.png" />
    </a>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    title: String,
    description: String,
    github: String,
    web: String,
  },
})
export default class Card extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.card {
  border-color: white;
  border-style: solid;
  border-width: 1px;
  border-radius: 5px;
  text-align: left;
  padding: 16px;
  margin: 8px;
  width: 100%;
  max-width: 500px;
  min-width: 300px;
  display: inline-block;
}

.icon:hover {
  border-width: 0px;
}

h2 {
  margin: 0;
}

a {
  margin-right: 8px;
}
</style>
