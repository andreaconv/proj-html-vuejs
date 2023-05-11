<script>
import firstSection from './partials/Build.vue';
import secondSection from './partials/Construct.vue';
import Dati from './partials/Dati.vue';
import Featured from './partials/Featured.vue';
import Learn from './partials/Learn.vue';
import Learnmb from './partials/Learnmobile.vue';

export default {
  name: 'Main',
  components: {
    firstSection,
    secondSection,
    Dati,
    Featured,
    Learn,
    Learnmb,
  },
}
</script>

<template>

  <firstSection />
  <secondSection />
  <Dati />
  <Featured />
  <Learn />
  <Learnmb />

</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;

</style>