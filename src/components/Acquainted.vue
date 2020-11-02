<template>
  <div class="acquainted container">
    <div class="main_content">
      <h2>Let's get acquainted</h2>
      <div class="content">
        <img class="content__img" src="../../public/img/man-laptop-v1.svg" alt="">
        <div class="content__text">
          <h3>I am cool frontend developer</h3>
          <p>
            We will evaluate how clean your approach to writing CSS and Javascript code is. You can use any CSS and Javascript 3rd party libraries without any restriction.
          </p>
          <p>
            If you don’t need HMR, feel free to leave Hot Middleware out of the packages listed above. The Dev Middleware does not depend on it.
          </p>
          <a class="content__link" href="#">Sing up now</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
@import "../../public/style/base";
  .acquainted {
    background-color: $background;
    .main_content {
      padding: 150px 60px 85px 60px;

      h2 {
        @extend .h1_desctop;
        text-align: center;
      }
    }
    .content {
      display: grid;
      grid-template-columns: 40% 60%;
      gap: 46px;
      padding-top: 60px;

      &__img {
        width: 100%;
        height: 300px;
      }
      &__text {
        h3 {
          @extend .h2;
          padding-bottom: 5px;
        }
        p {
          @extend .p;
          padding-bottom: 5px;
        }
        a {
          color: $red;
          font-weight: 500;
        }
      }
    }
  }
</style>