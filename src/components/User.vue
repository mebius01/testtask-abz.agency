<template>
  <li class="card">
    <img class="card__img" :src="object.photo" alt="">
    <a class="card__name h2" :href="object.id">
      {{object.name|cutName}}
      <span class="tooltips"
        v-if="object.name.length > 18">
        {{object.name}}
      </span>
    </a>
    <p class="card__prof">{{object.position}}</p>
    <a class="card__email" :href="'mailto:' + object.email">
      {{object.email|cutEmail}}
      <span class="tooltips" 
        v-if="object.email.length > 23">
        {{object.email}}
      </span>
    </a>
    <a class="card__tel" :href="'tel:' + object.phone">{{object.phone}}</a>
  </li>
</template>

<script>
  export default {
    props: {
      object: {
      type: Object,
        default: () => {
          return {}
        }
      }
    },
    filters: {
      cutEmail: (value) => {
        if (value.length > 23) {
          return value.slice(1, 20)+'...'
        } else {
          return value
        }
      },
      cutName: (value) => {
        if (value.length > 18) {
          return value.slice(1, 18)+'...'
        } else {
          return value
        }
      },
    }
  }
</script>



<style lang="scss" scoped>
  .card {
    width: 210px;
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
      position: relative;

      &:hover .tooltips {
        display: block;
        position: absolute;
        top: 50px;
        left: 50%;
        transform:translate(-50%, -50%);
      }
    }
    &__email {
      @extend .card__name;

      &:hover .tooltips {
        top: 30px;
      }
    }
    p, a {
      margin-bottom: 12px;
      color:  #44474A;
      text-align: center;
    }
      
  }
  .tooltips {
    display: none;
    background-color: #323231;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    z-index: 666;
  }
</style>