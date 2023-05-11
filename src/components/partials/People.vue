<script>
import {people} from '../../data/menu.js';

export default {
  name: 'People',
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
  
        <!-- TODO: aggiungere lo swiper e la persona mancante -->
        <div
          class="card rounded-0 text-center"
          v-for="(person,i) in people"
          :key="i">
          <img :src="`/testimonial-avata-0${i + 1}.jpg`" class="card-img-top">
          <p class="card-text">{{ person.description }}</p>
          <h5 class="card-title text-uppercase">{{person.name}}</h5>
          <span>{{person.profession}}</span>
        </div>
  
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
      padding: 80px 0;
      // overflow-x: scroll;

      .card{
        width: calc(30%);
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