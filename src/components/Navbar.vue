<template>
  <table class="nav">
    <tr>
      <td class="menu">
        <router-link to="/">Home</router-link>
        <router-link to="/skills">Skills</router-link>
        <router-link to="/projects">Projects</router-link>
      </td>
      <td class="title">
        <h1>
          <router-link to="/">
            <span class="mark">J</span>ULIEN D.
          </router-link>
        </h1>
      </td>
      <td class="icons">
        <a href="https://twitter.com/Shidoofficiel" target="_blank">
          <img width="16" src="twitter.png" />
        </a>
        <a href="https://www.twitch.tv/shidooo" target="_blank">
          <img width="16" src="twitch.png" />
        </a>
        <a href="https://discord.gg/zfAprJR" target="_blank">
          <img width="16" src="discord.png" />
        </a>
        <a href="https://github.com/Shidooo" target="_blank">
          <img width="16" src="github.png" />
        </a>
        <a href="mailto:julien@sukiyo.ch" target="_blank">
          <img width="16" src="mail.png" />
        </a>
      </td>
    </tr>
  </table>

  <div style="display: none;">
    Icons made by
    <a
      href="https://www.flaticon.com/authors/pixel-perfect"
      title="Pixel perfect"
    >Pixel perfect</a> from
    <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>
  </div>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';

export default class Navbar extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.nav {
  font-size: 14px;
  width: 100%;
  margin-bottom: 32px;
}

.nav td {
  width: 33.3%;
}

.nav .menu {
  @media (max-width: 768px) {
    text-align: center;
  }
}

.nav .menu a.router-link-exact-active {
  border-style: solid;
  border-width: 0 0 1px 0;
  border-color: #be2623;
  animation: borderFadeInAnimation ease 0.5s;
}

.nav .title {
  text-align: center;
  font-weight: normal;
  @media (max-width: 768px) {
    display: none;
  }
}

.nav .icons {
  text-align: right;
  @media (max-width: 768px) {
    display: none;
  }
}

a {
  margin-right: 32px;
}

.icons a:hover,
.title a:hover {
  border-width: 0px;
}
</style>
