<template>
  <div class="acquainted container">
    <div class="main_content">
      <h2>Our cheerful users</h2>
      <p>Attention! Sorting users by registration date</p>
      <ul class="content">
          <li v-for="item in users" :key="item.id">
            {{item}}
          </li>
      </ul>
      <User />
      <button class="content__btn">Show more</button>
    </div>
  </div>
</template>

<script>
import axios from "axios"
import User from "./User"
  export default {
    components: {
      User
    },
    data() {
      return {
        users: []
      }
    },
    created() {
      axios.get("https://frontend-test-assignment-api.abz.agency/api/v1/users?page=1&count=6")
        .then(response => {
          this.users = response.data.users
        })
        .catch(error => {
          console.log(error);
        })
    }
    
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
      grid-template-columns: repeat(auto-fit, minmax(200px, auto));
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