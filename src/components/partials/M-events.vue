<script>
import {cardsEvents} from '../../data/menu.js'

export default {
  name: 'events',
  data(){
    return{
      cardsEvents,
    }
  }
}
</script>

<template>
  <div class="ac-container">

    <div class="titles text-center">
      <h6>GET IN CONTACT NOW</h6>
      <h1>Upcoming <span>Events</span></h1>
    </div>

    <div class="row">

      <div
        class="col col-6 py-4"
        v-for="(date, i) in cardsEvents"
        :key="i">

        <div class="row mt-4">
          <div class="col col-8 px-5">
            <i class="fa-solid fa-location-dot me-2"></i> <span>{{date.city}}, {{date.state}}</span>
            <h5>{{date.plan}}</h5>
          </div>
          <div class="col col-4 text-center">
            <span id="day">{{date.day}}</span>
            <h5>{{date.month}}</h5>
          </div>
        </div>

        <div class="row justify-content-end">
          <div class="col col-4 text-center">
            <button type="button" class="btn my-2"><a href="#"><strong>Get ticket</strong></a></button>
          </div>
        </div>

      </div>

    </div>

    <div id="cta">
      <span>Excited about our event?</span>
      <a href="#">View all events <i class="fa-solid fa-arrow-right-long"></i></a>
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

    .col.col-6{
      border-radius: 6px;
      border-left: 4px solid white;

      &:hover{
        border-left: 4px solid $secondary-color;
      }
      &:hover button {
        background-color: $primary-color;
      }

      #day{
        color: $secondary-color;
        font-size: 3rem;
        line-height: 2rem;
      }

      button{
        background-color: $secondary-color;
        padding: .4rem 2rem;
        border: none;
        font-size: .8rem;
        
        *{
          color: white;
        }
      }
    }
    
    #cta{
      margin: 70px 0 80px;
      text-align: center;
      font-weight: bold;
      font-size: 1.1rem;
      span{
        color: $light-primary;
        margin-right: .5rem;
      }

      a{
        color: $secondary-color;
        &:hover{
          text-decoration: underline;
        }
      }
    }

  }

</style>