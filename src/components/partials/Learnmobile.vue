<script>

export default {
  name: 'Section Learn mobile',
}
</script>

<template>
  <section>
    <div class="ac-container h-100">
      <div class="row">

        <div id="pos-rel" class="col col-7 py-5">
          <img id="img" src="/home-5-image-02.png" alt="">
          <img id="shape" src="../../assets/img/underlay-shape-grey.svg" alt="">
          <img id="line" src="/maxcoach-shape-01.png" alt="">
          <div id="circle"></div>
          <img id="square" src="/maxcoach-shape-07.png" alt="">
        </div>

        <div class="col col-5 py-5">
          <div class="content-text">

            <div class="titles my-4">
              <h6>WHAT ARE YOU LOOKING FOR?</h6>
              <h1>Learn on your <span>mobile</span> anytime!</h1>
            </div>

            <p>Save lessons for later and revise or write notes at any time and on multiple devices on your way. Never interfere with activities of enjoyment or other precious moments. </p>

            <button type="button" class="btn my-4"><a href="#"><strong>Download Our App</strong></a></button>

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
    padding: 60px 0;

    #pos-rel{
      position: relative;

      img#img{
        position: absolute;
        left: 20%;
        top: 0;
        z-index: 6;
      }

      img#line{
        position: absolute;
        left: -20%;
        bottom: 50%;
        z-index: 3;
      }

      img#shape{
        position: absolute;
        right: 25%;
        bottom: -20%;
        width: 70%;
        z-index: 1;
      }

      div#circle{
        position: absolute;
        right: 10%;
        top: 10%;
        width: 60px;
        aspect-ratio: 1 / 1;
        border: 8px solid #ecc5ab;
        border-radius: 50%;
        z-index: 1;
      }

      img#square{
        position: absolute;
        right: 100px;
        bottom: 50px;
        z-index: 2;
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

      p{
        color: $gray;
      }

      button{
        background-color: $secondary-color;
        padding: .8rem 2.5rem;
        border: none;
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