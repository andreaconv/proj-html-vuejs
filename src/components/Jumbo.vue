<script>
export default {
  name: 'Jumbo',
}
</script>

<!-- FIXME: l'immagine di sfondo si vede -->

<template>
  <section>

    <!-- <img  id="jumbo" src="../../src/assets/img/jumbo-overlay.svg" alt=""> -->
    <div class="ac-container h-100">
      <div class="row">
        <div class="col col-6 d-flex flex-column justify-content-center">
          <div id="jumbotron">

            <h1>Complete Your Dreams in JavaS Programming</h1>
            <p class="my-5">Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.</p>
            <button type="button" class="btn ac"><a href="#"><i class="fa-solid fa-download"></i> Download free E-book</a></button>

          </div>
        </div>
        <div class="col col-6 py-5">
          <img  src="/home-5-hero-image.png" alt="">
        </div>
      </div>
    </div>

  </section>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/general' as *;
  @use '../scss/partials/vars' as *;

  section{
    background-color: $jumbo-color;
    padding-top: $height-header;

    // FIXME: una soluzione
    // background-image: url(../../src/assets/img/jumbo-overlay.svg);
    // background-repeat: no-repeat;
    // background-size: contain;
    // position: relative;

    // FIXME: altra soluzione
    // img#jumbo{
    //   position: absolute;
    //   bottom: 0;
    //   right: 0;
    //   width: 97%;
    //   height: 400px;
    //   transform: rotateX(180deg);
    // }

    // &:before {
    //   content: "";
    //   position: absolute;
    //   width: 97%;
    //   // height: 200%;
    //   bottom: 0;
    //   right: 0;
    //   // z-index: -1;
    //   background: url(../../src/assets/img/jumbo-overlay.svg) 0 0 repeat;
    //   transform: rotateX(180deg);
    // }

    #jumbotron{
      width: 70%;
      h1{
        font-size: 3rem;
        font-weight: bold;
        color: $primary-color;
      }
      p{
        font-size: 1.1rem;
        color: $light-primary;
        line-height: 2rem;
      }
      button.btn.ac{
        background-color: $secondary-color;
        padding: .8rem 2.4rem;
        border: none;
        cursor: pointer;
        &:hover{
          background-color: $primary-color;
        }

        *{
          color: white;
        }
      }
    }
  }

</style>