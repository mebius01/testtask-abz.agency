<template>
  <div id="app">
    <Header />
    <Banner />
    <Acquainted />
    <Users />
    <Registration />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header"
import Banner from "./components/Banner"
import Acquainted from "./components/Acquainted"
import Users from "./components/Users"
import Registration from "./components/Registration"
import Footer from "./components/Footer"
export default {
  name: "App",
  components: {
    Header,
    Banner,
    Acquainted,
    Users,
    Registration,
    Footer
  }
};
</script>

<style lang="scss">
// @import "normalize-scss";
// @include normalize();
@import "../node_modules/reset-css/sass/_reset";
@import "../public/style/base";
* {
  box-sizing: border-box
}
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
