<script>
import firstSection from './partials/Build.vue';
import secondSection from './partials/Construct.vue';
import Dati from './partials/Dati.vue';
import Featured from './partials/Featured.vue';
import Learn from './partials/Learn.vue';
import Learnmb from './partials/Learnmobile.vue';
import Events from './partials/M-events.vue';
import People from './partials/People.vue';

export default {
  name: 'Main',
  components: {
    firstSection,
    secondSection,
    Dati,
    Featured,
    Learn,
    Learnmb,
    Events,
    People,
  },
}
</script>

<template>

  <!-- TODO: potrei passare i titoli delle varie sezioni con delle props -->

  <firstSection />
  <secondSection />
  <Dati />
  <Featured />
  <Learn />
  <Learnmb />
  <Events />
  <People />

</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;

</style>