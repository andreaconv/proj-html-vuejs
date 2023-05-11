<script>
import {people} from '../../data/menu.js';

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Pagination } from 'swiper';

export default {
  name: 'People',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
  data(){
    return{
      people,
    }
  }
}
</script>

<template>
  <section>
    <div class="ac-container">

      <div class="titles text-center">
        <h6>PEOPLE ARE PRAISING MAXCOACH</h6>
        <h1>What make they <span>love us?</span></h1>
      </div>

      <div class="cards-wrapper d-flex">

        <swiper
          :spaceBetween="0"
          :slidesPerView="3"
          :loop="Infinity"
          :pagination="{
            clickable: true,
          }"
          :modules="modules"
          class="mySwiper"
        >
          <swiper-slide 
          v-for="(person,i) in people"
          :key="i">
            <div class="card rounded-0 text-center">
              <img :src="`/testimonial-avata-0${i + 1}.jpg`" class="card-img-top">
              <p class="card-text">{{ person.description }}</p>
              <h5 class="card-title text-uppercase">{{person.name}}</h5>
              <span>{{person.profession}}</span>
            </div>
          </swiper-slide>
        </swiper>
  
      </div>
      
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  section{
    background-color: $third-white;
  }
  .ac-container{
    padding-top: 120px;
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
      // padding: 80px 0;
      .mySwiper{
        padding: 100px 0 ;

        // FIXME: non riesco a cambiare le dimensioni dei pallini
        .swiper-pagination-bullet{
          height: 12px !important;
          width: 12px !important;
        }
      }

      .card{
        // width: calc(30%);
        margin: 0 1rem;
        padding: 100px 2rem 3rem;
        position: relative;
        border: none;
        box-shadow: 0px 0px 10px $light-primary;
        img{
          position: absolute;
          top: 0;
          left: 50%;
          transform: translate(-50%, -50%);
          border-radius: 50%;
          width: 40%;
        }
        p{
          color: $primary-color;
          font-size: 1.1rem;
          font-weight: 600;
        }
        span{
          color: $gray;
        }
      }
    }
  }

</style>