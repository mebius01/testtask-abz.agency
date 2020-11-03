<template>
  <div id="app">
    <Header />
    <Banner />
    <Acquainted />
    <Users />
    <Registration />
  </div>
</template>

<script>
import Header from "./components/Header"
import Banner from "./components/Banner"
import Acquainted from "./components/Acquainted"
import Users from "./components/Users"
import Registration from "./components/Registration"
export default {
  name: "App",
  components: {
    Header,
    Banner,
    Acquainted,
    Users,
    Registration
  }
};
</script>

<style lang="scss">
// @import "normalize-scss";
// @include normalize();
@import "../node_modules/reset-css/sass/_reset";
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
