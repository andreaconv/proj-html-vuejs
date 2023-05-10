<script>
import mySection from './partials/mySection.vue';
import Sectionjumbo from './partials/Sectionjumbo.vue';
import Dati from './partials/Dati.vue';

export default {
  name: 'Main',
  components: {
    mySection,
    Sectionjumbo,
    Dati,
  },
}
</script>

<template>

  <mySection />
  <Sectionjumbo />
  <Dati />

</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;

</style>