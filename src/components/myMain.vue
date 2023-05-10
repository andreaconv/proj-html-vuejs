<script>
import firstSection from './partials/Build.vue';
import secondSection from './partials/Construct.vue';
import Dati from './partials/Dati.vue';
import Featured from './partials/Featured.vue';

export default {
  name: 'Main',
  components: {
    firstSection,
    secondSection,
    Dati,
    Featured,
  },
}
</script>

<template>

  <firstSection />
  <secondSection />
  <Dati />
  <Featured />

</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;

</style>