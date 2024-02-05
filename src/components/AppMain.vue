<script>
import PokemonCard from "./PokemonCard.vue";
export default {
  name: "AppMain",
  components: { PokemonCard }
}

</script>

<template>
  <div class="container bg-danger">
    <div class="row row-cols-5 p-5 d-flex justify-content-between flex-wrap g-5">
      <!-- COL -->
      <div class="col p-2">
        <PokemonCard />
      </div>
      <!-- COL -->
    </div>
  </div>
</template>

<style scoped>
.row {
  margin-top: 100px;
  background-color: #DEDEDE;
  border-radius: 30px;
}
</style>
