<template>
  <div class="reg container">
    <div class="main_content">
      <h2>Register to get a work</h2>
      <p>Attention! After successful registration and alert, update the list of users in the block from the top</p>
      <form action="" class="form">
        <label for="name">Name
        <input type="text" name="name">
</label>
        <label for="email">EMail
        <input type="email" name="email">
</label>
        <label for="tel">Phone
        <input type="tel" name="tel">
</label>
        <input type="checkbox" name="" id="">
        <label for="">Front Ebd</label>

        <input type="file" name="" id="">
      </form>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
@import "../../public/style/base";
  .reg {
    background-color: $background;
    display: flex;
    justify-content: center;
    
    .main_content {
      padding: 150px 60px 85px 60px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      border: 1px solid;

      h2 {
        @extend .h1_desctop;
        text-align: center;
        width: 540px;
      }
      p {
        text-align: center;
        width: 450px;
      }
    }
    .form {
            display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  }
</style>