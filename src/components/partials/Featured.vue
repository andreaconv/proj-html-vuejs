<script>
export default {
  name: 'Featured',
}
</script>

<template>
  <section>

    <div class="ac-container">
  
      <div class="titles text-center">
        <h6>CHOOSE WHERE YOU'D LIKE TO BEGIN</h6>
        <h1>Latest Featured <span>Courses</span></h1>
      </div>
  
      <div class="cards-wrapper d-flex flex-wrap">
  
        <!-- TODO: da ciclare le cards -->
  
        <div class="card p-3">
          <strong id="price">free</strong>
          <div class="image">
            <img src="/stock-full-hd-01-480x298.jpg" class="card-img-top" alt="...">
          </div>
          <div class="card-body px-4">
            <img id="profile" src="/profile-01.jpeg" alt="">
            <span id="name">Owen Christ</span>
            <h4 class="card-title ">Personal finance: financial security thinkine princels</h4>
            <div class="info">
              <span><i class="fa-solid fa-sheet-plastic"></i> 2 lessons</span>
              <span><i class="fa-regular fa-user"></i> 249 students</span>
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
    background-color: $second-white;
  }
  .ac-container{
    padding: 0;
    .titles{
      padding: 60px 0;
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

    .card{
      width: calc(100% / 3);
      border: none;
      position: relative;
      .image{
        overflow: hidden;

        img{
          transition: all 0.8s ease;
        }
      }
      &:hover .image img{
        transform: scale(1.1);
      }

      &:hover h4{
        color: $secondary-color;
      }

      strong#price{
        position: absolute;
        top: 1rem;
        right: 1rem;
        padding: 0.3rem 1.5rem;
        font-size: 1.2rem;
        color: white;
        border-radius: 0 6px 0 6px;
        z-index: 1;
        background-color: $secondary-color;
      }

      img#profile{
        border-radius: 50%;
        margin-right: 1rem;
      }

      span#name{
        color: $gray;
      }

      h4{
        margin: 1rem 0;
      }

      .info{
        margin-top: 2rem ;
        color: $gray;

        span{
          margin-right: 1rem;
        }
        
        i.fa-sheet-plastic{
          transform: rotateX(180deg);
        }
      }
    }
  }

</style>