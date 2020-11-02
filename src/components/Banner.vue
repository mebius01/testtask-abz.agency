<template>
  <div class="banner container">
    <div class="content">
      <h1 class="content__title">
        {{title}}
      </h1>
      <p class="content__text">
        {{text}}
      </p>
      <button class="content__btn">test test</button>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: "Test assignment for Frontend Developer position",
        text: "We kindly remind you that your test assignment should be submitted as a link to github/bitbucket repository. Please be patient, we consider and respond to every application that meets minimum requirements. We look forward to your submission. Good luck! The photo has to scale in the banner area on the different screens"
      }
    },
  }
</script>

<style lang="scss" scoped>
@import "../../public/style/base";
  .banner {
    height: 595px; // !!
    background-image: url("../../public/img/banner-photo.jpg");
    background-size: cover;

    .content {
      padding: 106px 468px 112px 30px;
      color: white;

      &__title {
        @extend .h1_desctop;
        text-transform: uppercase;
      }

      &__text {
        @extend .p;
      }

      &__btn {
        @extend  .btn;
      }
    }
  }
</style>