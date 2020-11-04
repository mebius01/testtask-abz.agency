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
          <div class="field">
            <span>{{value}}</span>
            <label>
              <input type="file" name="file" @change="handleFileChange" ref="myFiles" accept=".jpg, .jpeg, .png"/>
                Browse
            </label>
          </div>
        </div>
        <hr>
        <button class="btn">Sing up now</button>
      </form>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        value: "Upload your photo"
      }
    },
    methods: {
      handleFileChange() {
        this.value = this.$refs.myFiles.files[0].name
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

      h2 {
        @extend .h1_desctop;
        text-align: center;
        width: 540px;
        margin-bottom: 20px;
      }
      p {
        color: #44474A;
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
        color: #44474A;
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
      .file {

        .field {
          @extend input;
          position: relative;
          
          span {
            color: #CCC;
            position: absolute;
            top:5px;
            left: 15px;
          }

          input[type="file"] {
            display: none;
          }
          label {
            position: absolute;
            top:0;
            right: 0;
            background-color: #F8F7F5;
            height: 32px;
            text-align: center;
            padding: 6px 10px;
            cursor: pointer;
          }
        }
        
      }
      .input{
        display: flex;
        flex-direction: column;
      }
      .file {
        margin-top: 35px;
      }
    }
  }
</style>