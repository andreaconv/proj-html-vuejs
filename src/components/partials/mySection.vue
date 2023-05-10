<script>
import { aboutUs } from '../../data/menu.js'
export default {
  name: 'section',
  data(){
    return{
      aboutUs
    }
  }
}
</script>

<template>
  <div class="ac-container">
    <div class="titles text-center">
      <h6>START LEARNING CODING LANGUAGES</h6>
      <h1>Build Your Dream <span>TODAY</span></h1>
    </div>
    <div class="cards-wrapper d-flex">

      <div
        class="card"
        v-for="(item, index) in aboutUs"
        :key="index">
        <img :src="`/home-5-image-box-0${index + 1}.png`" class="card-img-top">
        <div class="card-body text-center">
          <h5 class="card-title">{{item.title}}</h5>
          <p class="card-text">{{item.description}}</p>
          <a href="#" class="btn ">Start now <i class="fa-solid fa-arrow-right-long"></i></a>
        </div>
      </div>

    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  .ac-container{

    .titles{
      padding: 60px 0;
      h6{
        color: $gray;
      }
  
      h1{
        color: $primary-color;
        font-weight: bold;
        font-size: 3rem;
        span{
          color: $secondary-color;
          font-weight: 400;
        }
      }
    }
    .cards-wrapper{
      // padding: 60px 0;
      .card{
        width: calc(100% / 4);
        border: none;

        &:hover a{
          color: $secondary-color;
        }

        img{
          width: 60%;
          height: 40%;
          margin: 0 auto;
        }
        p{
          color: $gray;
        }
        a{
          color: $light-primary;
          font-weight: bold;
        }
      }
    }
  }

</style>