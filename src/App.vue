<script>
import Header from './components/myHeader.vue';
import Main from './components/myMain.vue';
import Footer from './components/myFooter.vue';
import { store } from './data/store';

export default {
  name: 'App',
  components: {
    Header,
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

  <Header />
  <Main />
  <Footer />

</template>

<style lang="scss">
  @use './scss/main.scss';
</style>