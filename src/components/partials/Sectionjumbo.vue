<script>
export default {
  name: 'Sectionjumbo',
}
</script>

<template>
  <section>
    <div class="ac-container h-100">
      <div class="row">
        <div class="col col-6 py-5">
          <img  src="/about-us-03-image-01.png" alt="">
        </div>
        <!-- d-flex flex-column justify-content-center -->
        <div class="col col-6 py-5">
          <div class="content-text">

            <div class="titles">
              <h6>DREAM WITH <strong>MAXCOACH</strong></h6>
              <h1>Construct A <span>Stunning</span> Career Perspective</h1>
            </div>

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
    // debug
    background-color: $jumbo-color;

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