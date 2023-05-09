<script>
export default {
  name: 'Search',
}
</script>

<!-- TODO: 
  1. togliere il bordo blu quando viene selezionato l'input
  2. togliere il bordo sinistro all'icona di ricerca -->

<template>
  <div class="input-group">
    <input type="text" class="form-control px-3 p-2" placeholder="Search.." aria-label="Example text with button addon" aria-describedby="button-addon1">
    <button class="btn btn-outline-secondary" type="button" id="button-addon1"><i class="fa-solid fa-magnifying-glass"></i></button>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../scss/partials/vars' as *;
  @use '../../scss/partials/general' as *;

.input-group{
    width: auto;

    input{
      border: 1px solid $secondary-color;
      box-shadow: none;
    }

    .btn-outline-secondary{
      border: 1px solid $secondary-color;
      color: $secondary-color;
      background-color: white;

      &:hover{
        background-color: $secondary-color;
        color: white;
      }
    }
  }

</style>