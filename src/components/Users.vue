<template>
  <div class="acquainted container">
    <div class="main_content">
      <h2>Our cheerful users</h2>
      <p>Attention! Sorting users by registration date</p>
      <div class="content">
        <p class="user">1</p>
        <p class="user">2</p>
        <p class="user">3</p>
        <p class="user">4</p>
        <p class="user">5</p>
        <p class="user">6</p>
      </div>
      <button class="content__btn">Show more</button>
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
    background-color: $background_g;
    .main_content {
      padding: 150px 80px;

      h2 {
        @extend .h1_desctop;
        text-align: center;
      }
      p {
        color: #595857;
        text-align: center;
      }
    }
    .content {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, auto));
      justify-items: center;
      gap: 30px;
      padding-top: 50px;

      .user {
        width: 210px;
        height: 280px;
        background: rgb(243, 145, 145);
      }
    }
    button {
      @extend .btn;
      margin: 0 auto;
    }
  }
</style>