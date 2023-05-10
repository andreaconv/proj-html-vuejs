<script>
import mySection from './partials/mySection.vue';
import Sectionjumbo from './partials/Sectionjumbo.vue';

export default {
  name: 'Main',
  components: {
    mySection,
    Sectionjumbo,
  },
}
</script>

<template>

  <mySection />
  <Sectionjumbo />

</template>

<style lang="scss" scoped>
  @use '../scss/partials/vars' as *;

</style>