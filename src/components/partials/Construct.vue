<script>
import Accordion from './myAccordion.vue';

export default {
  name: 'Sectionjumbo',
  components: {
    Accordion,
  },
}
</script>

<template>
  <section>
    <div class="ac-container h-100">
      <div class="row">
        <div id="pos-rel" class="col col-6 py-5">
          <img id="img" src="/about-us-03-image-01.png" alt="">
          <img id="shape" src="../../assets/img/underlay-shape-lilla.svg" alt="">
        </div>

        <div class="col col-6 py-5">
          <div class="content-text">

            <div class="titles my-5">
              <h6>DREAM WITH <strong>MAXCOACH</strong></h6>
              <h1>Construct A <span>Stunning</span> Career Perspective</h1>
            </div>

            <Accordion />

          </div>
        </div>
      </div>
    </div>

  </section>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  section{
    #pos-rel{
      position: relative;

      img#img{
        position: absolute;
        left: 0;
        top: 0;
      }

      img#shape{
        width: 60%;
      }
    }
    .content-text{
      .titles{
        h6{
          color: $gray;
        }
        h1{
          color: $primary-color;
          font-weight: bold;
          font-size: 3rem;
          span{
            color: $secondary-color;
            font-weight: 400;
          }
        }
      }
    }
  }
</style>