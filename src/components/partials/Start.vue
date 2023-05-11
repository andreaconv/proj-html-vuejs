<script>
import {cardsFeatured} from '../../data/menu.js';

export default {
  name: 'Featured',
  data(){
    return{
      cardsFeatured,
    }
  }
}
</script>

<template>
  <section>
    
    <div class="ac-container">
      <div id="circle"></div>
      <img id="line" src="/maxcoach-shape-01.png" alt="">
      <img id="semicircle" src="/maxcoach-shape-02.png" alt="">
  
      <div class="titles text-center">
        <h4>Start today for getting <span>Online Certification</span></h4>
        <h2><strong>You can be your own guiding star with our help!</strong></h2>
      </div>

      <div class="text-center">
        <button type="button" class="btn"><a href="#"><strong>Get started now</strong></a></button>
      </div>
    </div>

  </section>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  section{
    background-color: $second-white;
    padding: 60px 0;
  }
  .ac-container{
    padding: 0;
    position: relative;

    div#circle{
      position: absolute;
      left: 10%;
      top: 0;
      width: 60px;
      aspect-ratio: 1 / 1;
      border: 8px solid #ecc5ab;
      border-radius: 50%;
    }
  
    img#line{
      position: absolute;
      left: 0;
      bottom: 40%;
    }
  
    img#semicircle{
      position: absolute;
      right: 0;
      bottom: 0;
    }
    .titles{
      padding: 30px 0;
  
      h4{
        color: $primary-color;
        font-weight: bold;
        font-size: 1.5rem;
        span{
          color: $secondary-color;
          font-weight: 400;
        }
      }

      h2{
        color: $primary-color;
      }
    }

    button{
      background-color: $secondary-color;
      padding: .8rem 4rem;
      border: none;
      &:hover{
        background-color: $primary-color;
      }
      
      *{
        color: white;
      }
    }
  }

</style>