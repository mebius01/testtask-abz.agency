<template>
  <div class="reg container">
    <div class="main_content">
      <h2>Register to get a work</h2>
      <p>Attention! After successful registration and alert, update the list of users in the block from the top</p>
      <form class="form">
        <div class="input">
          <label for="name">Name</label>
          <input placeholder="Your name" type="text" name="name">
          <label for="email">Email</label>
          <input placeholder="Your email" type="email" name="email">
          <label for="tel">Phone number</label>
          <input placeholder="+380 XX XXX XX XX" type="tel" name="tel">
        </div>
        <div class="radio">
          <p>
            <input type="radio" name="prof"><label for="front">Frontend developer</label>
          </p>
          <p>
          <input type="radio" name="prof"><label for="back">Backend developer</label>
          </p>
          <p>
          <input type="radio" name="prof"><label for="des">Designer</label>
          </p>
          <p>
          <input type="radio" name="prof"><label for="qa">QA</label>
          </p>
        </div>
        <div class="file">
          <label for="file">Photo</label>
          <input type="file" name="file" @change="handleFileChange" ref="myFiles" accept=".jpg, .jpeg, .png">
        </div>
        <button class="btn">Sing up now</button>
      </form>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      handleFileChange() {
        console.log(this.$refs.myFiles.files[0].name);
      }
    }
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
        margin-bottom: 20px;
      }
      p {
        color: #696868;
        text-align: center;
        line-height: 23px;
        width: 463px;
        margin-bottom: 30px;
      }
    }
    .form {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      input {
        box-sizing: border-box;
        width: 463px;
        height: 34px;
        border: 2px solid #E9ECEE;
        border-radius: 5px;
        padding: 12px;
        font-size: 16px;
        font-weight: 500;
        margin-bottom: 35px;
        margin-top: 12px;
        outline: none;
        &::placeholder {
          color: #D0D4D9;
        }
      }
      label {
        font-size: 16px;
        font-weight: 500;
        color: #44474A;
      }
      p {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        margin: 0;
        input[type=radio] {
          width: 19px;
          margin: 0;
        }
        label {
          margin-left: 8px;
        }
      }
      input[type=file] {
        padding: 0;
        text-align: center;
      
        &::-webkit-file-upload-button {
          background-color: #F8F7F5;
          border: none;
          border-left: 1px solid #D0D4D9;
          height: 30px;
          float: right;
          outline: none;
        }
      }
      .input, .file {
        display: flex;
        flex-direction: column;
      }
      .file {
        margin-top: 35px;
      }
    }
  }
</style>