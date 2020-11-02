<template>
  <div id="app">
    <Header />
    <Banner />
    <Acquainted />
    <Users />
  </div>
</template>

<script>
import Header from "./components/Header"
import Banner from "./components/Banner"
import Acquainted from "./components/Acquainted"
import Users from "./components/Users"
export default {
  name: "App",
  components: {
    Header,
    Banner,
    Acquainted,
    Users
  }
};
</script>

<style lang="scss">
@import "normalize-scss";
@include normalize();
@import "../public/style/base";
html {
  margin: 0;
  box-sizing: border-box;
  font-family: 'Open Sans', sans-serif;
  font-weight: 400;
  color: #212529;

  background-color: grey;
}
#app {}
</style>
