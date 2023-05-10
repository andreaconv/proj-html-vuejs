<script>
export default {
  name: 'accordion',
}
</script>

<!-- TODO:  
  togliere il bordino al bottom di ogni riga
  bordi arrotondati anche al click
  cambiare l'icona della freccia col + -->
<template>
  <div class="accordion accordion-flush" id="accordionFlushExample">

    <div class="accordion-item">
      <h2 class="accordion-header">
        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseOne" aria-expanded="false" aria-controls="flush-collapseOne">
          Multiple Platforms Supported for Teaching & Studying
        </button>
      </h2>
      <div id="flush-collapseOne" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
        <div class="accordion-body">MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren’t supposed to be devoured in a short time, you can always access our knowledge base from any device. </div>
      </div>
    </div>

    <div class="accordion-item">
      <h2 class="accordion-header">
        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseTwo" aria-expanded="false" aria-controls="flush-collapseTwo">
          Multiple Course Participation at the Same Time
        </button>
      </h2>
      <div id="flush-collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
        <div class="accordion-body">Study for a number of courses at the same time is possible as long as you can afford the fee and time for completing them in the proper time. Learn at your own desired timeline and timetable. Maximum up to 5 course at a time for a learner at MaxCoach.</div>
      </div>
    </div>

    <div class="accordion-item">
      <h2 class="accordion-header">
        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseThree" aria-expanded="false" aria-controls="flush-collapseThree">
          Track Study Progress & Deliver Prompt Feedback
        </button>
      </h2>
      <div id="flush-collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionFlushExample">
        <div class="accordion-body">It’s not just a normal thing to be able to build such a solid online educational system like MaxCoach where your progress is easily tracked and feedback is properly delivered. We promise to keep improving our system for better stability and flexibility. </div>
      </div>
    </div>

  </div>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

  .accordion-item{
    margin: 2rem 0;
    .accordion-header{
      button{
        box-shadow: none;
        font-weight: bold;
        color: $gray;
        &:hover{
          background-color: $secondary-color;
          color: $first-white;
        }
      }
      // .accordion-button.collapsed{
      //   border-radius: 8px;
      // }
    }
    .accordion-body{
      color: $light-primary;
    }
  }

</style>