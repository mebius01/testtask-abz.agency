<template>
  <div class="card">
    <img class="card__img" src="../../public/img/photo-cover.png" alt="">
    <h3 class="card__name h2">Jon Dowe</h3>
    <p class="card__prof">Frontend developer</p>
    <p class="card__email">test@gmail.com</p>
    <p class="card__tel">+380 50 124 58 74</p>
  </div>
</template>

<script>
  export default {
    props: {
      
    }
  }
</script>

<style lang="scss" scoped>
  .card {
    // border: 1px solid;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    
    &__img {
      border-radius: 50%;
      width: 72px;
      height: 72px;
      margin-bottom: 20px;
    }
    &__name {
      margin-bottom: 17px;
    }
    p {
      margin-bottom: 12px;
      color:  #44474A;
    }
  }
</style>