<template>
  <header>
    <nav>
      <a href="/" class="logo"><img :src="logo.src" :alt="logo.title"></a>
      <ul class="menu">
        <li class="menu__item" v-for="(item, index) in menu" :key="index" >
          <a :href="item.href" class="menu__link">{{item.title}}</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
import logo from "../../public/img/logo.svg"
  export default {
    data() {
      return {
        logo: {title: "Test Task", src: logo},
        menu: [
          {title: "About me", href: "#"},
          {title: "Relationships", href: "#"},
          {title: "Requirements", href: "#"},
          {title: "Users", href: "#"},
          {title: "Sign Up", href: "#"},
        ]
      }
    },
  }
</script>

<style lang="scss" scoped>
@import "../../public/style/base";
  header {
    @extend .container;
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: $background;
    @extend .padding;

    ul {
      list-style: none;
      display: flex;

      li {
        margin-left: 28px;
      }
    }
  }
</style>