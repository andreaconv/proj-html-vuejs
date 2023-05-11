<script>

export default {
  name: 'Section Learn pc',
}
</script>

<template>
  <section>
    <div class="ac-container h-100">
      <div class="row">

        <div class="col col-6 py-5">
          <div class="content-text">

            <div class="titles my-4">
              <h6>WHY HESITATE TO REGISTER?</h6>
              <h1>Learn At Your <br> Own <span>Pace</span></h1>
            </div>

            <ul>
              <li><i class="fa-solid fa-check"></i> Select & customize courses to your preferences</li>
              <li><i class="fa-solid fa-check"></i> Change the tutor and make arrangements</li>
              <li><i class="fa-solid fa-check"></i> Participate in events to join others</li>
              <li><i class="fa-solid fa-check"></i> Get the desired certificate delivered at house</li>
            </ul>

            <button type="button" class="btn my-4"><a href="#"><strong>Get started for free</strong></a></button>

          </div>
        </div>
        
        <div id="pos-rel" class="col col-6 py-5">
          <img id="img" src="/home-5-image-01.png" alt="">
          <img id="shape" src="../../assets/img/underlay-shape-grey.svg" alt="">
          <img id="dots" src="/maxcoach-shape-05.png" alt="">
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

      ul{
        li{
          color: $gray;
          i{
            color: $secondary-color;
            margin: 0.8rem 0.8rem 0.8rem 0;
          }
        }
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


    #pos-rel{
      position: relative;

      img#img{
        position: absolute;
        left: 0;
        top: 0;
        z-index: 3;
      }

      img#shape{
        position: absolute;
        left: -50px;
        bottom: -50px;
        width: 80%;
        z-index: 2;
      }

      img#dots{
        position: absolute;
        right: 100px;
        bottom: 100px;
        z-index: 1;
      }
    }
    
  }
</style>