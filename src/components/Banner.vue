<template>
  <div class="banner container">
    <div class="content">
      <h1 class="content__title">
        Test assignment for Frontend Developer position
      </h1>
      <p class="content__text">
        We kindly remind you that your test assignment should be submit
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, explicabo sunt, nemo minima accusantium ea repellat quibusdam quasi cumque magni eligendi debitis, deserunt dolores expedita soluta inventore ipsum delectus eos.
      </p>
      <button class="content__btn">test test</button>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
@import "../../public/style/base";
  .banner {
    height: 595px; // !!
    background-image: url("../../public/img/banner-photo.jpg");
    background-size: cover;

    .content {
      padding: 106px 478px 112px 30px;
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