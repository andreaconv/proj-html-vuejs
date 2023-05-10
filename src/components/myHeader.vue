<script>
import Nav from './partials/myNav.vue'

export default {
  name: 'Header',
  components: {
    Nav,
  },
  methods: {
    
  }
}
</script>

<!-- TODO: MODIFICARE HEADER
  1. fixare in alto 
  2. cambiare il colore di sfondo
  3. aggiungere border shadow-->
<template>
  <header>

    <div class="ac-container d-flex align-items-center justify-content-between h-100">
      <a href="#"><img src="/dark-logo.png" alt="logo"></a>
      <Nav />
    </div>

  </header>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;
  @use '../scss/partials/general' as *;

  header{
    height: $height-header;
    background-color: $jumbo-color;
    position: fixed;
    z-index: 999;
    top: 0;
    right: 0;
    width: 100%;

    .ac-container{

      a img{
        height: 25px;
      }
    }
  }

</style>