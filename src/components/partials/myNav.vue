<script>
import Search from './mySearch.vue';
import { headerMenu } from '../../data/Header-menu.js'

export default {
  name: 'Nav',
  components: {
    Search,
  },
  data(){
    return{
      headerMenu,
    }
  }
}
</script>

<!-- TODO: aggiungere il menu a tendina ad ogni elemento del menu -->
<template>
  <nav class="d-flex align-items-center h-100">
    <ul class="menu d-flex align-items-center h-100">
      <li
        v-for="(item, index) in headerMenu"
        :key="index"><a
        :href="item.link">{{item.text}}
        <span></span></a></li>
    </ul>
    <!-- TODO: aggiungere il numero sul carrello -->
    <ul class="options d-flex align-items-center h-100">
      <li><a href="#"><i class="fa-solid fa-cart-shopping me-2"></i></a></li>
      <li><a href="#"><i class="fa-regular fa-circle-user mx-3"></i></a></li>
    </ul>
    <Search />
  </nav>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  nav{

    ul.menu{
      font-weight: bold;

      li{
        margin: 0 1.5rem;

        // TODO: aggiustare l'hover più fluido e la barra sotto più lunga che prenda anche la chevron
        &:hover *{
          color: $secondary-color;
          text-decoration: underline;
        }

        a{
          color: $primary-color;

          span{
            position: relative;
            margin-left: 0.3rem;

            &::after{
              content: '\f078';
              font-family: 'fontawesome';
              font-size: 0.5rem;
              position: absolute;
              top: 50%;
              transform: translate(0, -50%);
            }
          }
        }
      }
    }

    ul.options{

      li{

        a{
          color: #333333;

          &:hover{
            color: $secondary-color;
          }
        }
      }
    }

  }


</style>