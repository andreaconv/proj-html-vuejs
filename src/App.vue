<script>
import Header from './components/myHeader.vue';
import Jumbo from './components/Jumbo.vue';
import Main from './components/myMain.vue';
import Footer from './components/myFooter.vue';
import { store } from './data/store';

export default {
  name: 'App',
  components: {
    Header,
    Jumbo,
    Main,
    Footer,
  },
  data(){
    return {
      store,
    }
  },
  methods: {
    show(){
      store.showString = 'Hello'
      console.log(store.showString)
    }
  },
  mounted(){
    this.show()
  }
}
</script>

<template>

  <div>

    <Header />
    <Jumbo />
    <Main />
    <Footer />
    
  </div>

</template>

<style lang="scss">
  @use './scss/main.scss';
  
</style>