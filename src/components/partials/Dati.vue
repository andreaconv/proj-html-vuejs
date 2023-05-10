<script>
import {dati} from '../../data/menu.js'
export default {
  name: 'Dati',
  data(){
    return{
      dati,
    }
  }
}
</script>

<template>
  <main>
    <div class="ac-container">
      <div class="row">
        <div
          class="col col-3 text-center"
          v-for="(item, index) in dati"
          :key="index">
          <h1>{{item.num}}</h1>
          <h6>{{item.text}}</h6>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  main{
    padding: 60px 0;
    background-color: $third-white;

    h1{
      color: $secondary-color;
      font-weight: bold;
    }
  }

</style>