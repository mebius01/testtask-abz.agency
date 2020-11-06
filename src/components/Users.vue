<template>
  <div class="acquainted container">
    <div class="main_content">
      <h2>Our cheerful users</h2>
      <p>Attention! Sorting users by registration date</p>
      <ul class="content">
        <User v-for="item in users"
          :key="item.id"
          :object="item" />
      </ul>

      <button class="content__btn"
        @click="updateUsers"
        v-if="links.next_url"
        >Show more
      </button>
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
        users: [],
        data: [],
        count: 6,
        page: 1,
        links: null,
        url: "https://frontend-test-assignment-api.abz.agency/api/v1"
      }
    },
    methods: {
      getUsers() {
        axios.get(`${this.url}/users?page=${this.page}&count=${this.count}`)
        .then(response => {
          this.data = response.data
          this.links = this.data.links
          this.users = this.data.users
        })
        .catch(error => {
          console.log(error);
        })
      },
      updateUsers() {
        this.count = this.count + 6
        this.getUsers()
      }
    },
    created() {
      this.getUsers()
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