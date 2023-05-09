<script>
import { exploreMenu } from '../data/menu.js'
import { infoMenu } from '../data/menu.js'

export default {
  name: 'Footer',
  data(){
    return{
      exploreMenu,
      infoMenu
    }
  }
}
</script>

<!-- TODO: animazione smooth per l'hover di tutti i link -->

<template>
  <div class="ac-container px-2">
    <section>
      <div class="row">

        <div class="col col-6">
          <h5>Address</h5>
          <ul id="address">
            <li>382 NE 191st St # 87394 Miami, FL 33179-3899</li>
            <li>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</li>
            <li><a href="#">support@maxcoach.com</a></li>
          </ul>
          <div class="social">
            <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
            <a href="#"><i class="fa-brands fa-twitter mx-4"></i></a>
            <a href="#"><i class="fa-brands fa-instagram me-4"></i></a>
            <a href="#"><i class="fa-brands fa-linkedin"></i></a>
          </div>
        </div>

        <div class="col col-3">
          <h5>Explore</h5>
          <ul class="d-flex flex-wrap menu">
            <li
              v-for="(item, index) in exploreMenu"
              :key="index"><a
              :href="item.link">{{item.text}}</a></li>
          </ul>
        </div>

        <div class="col col-3">
          <h5>Information</h5>
          <ul class="menu">
            <li
              v-for="(item, index) in infoMenu"
              :key="index"><a
              :href="item.link">{{item.text}}</a></li>
          </ul>
        </div>

      </div>
    </section>
    <section>
      <div class="row">
        <div class="text-center">© 2020 Maxcoach. All Rights Reserved</div>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;
  @use '../scss/partials/general' as *;

  .ac-container{
    padding-top: 70px;

    section{
      margin-bottom: 50px;
    }

    h5{
    font-weight: bold;
    margin-bottom: 0.6rem ;
    }

    ul#address{
      li{
        margin-bottom: 0.6rem;
        font-size: 0.9rem;
        color: $gray;
      }
    }

    .social{
      margin-top: 1.5rem;
      i{
        font-size: 1.5rem;
        color: $light-gray;
        &:hover{
          color: $secondary-color;
        }
      }
    }

    a{
      color: $gray;
      &:hover{
        color: $secondary-color;
      }
    }

    ul.menu{
      li{
        flex: 1 1 50%;
        margin-bottom: 0.6rem ;
        font-size: 0.9rem;
      }
    }

    .text-center{
      font-size: .9rem;
      color: $light-gray;
    }
  }

</style>