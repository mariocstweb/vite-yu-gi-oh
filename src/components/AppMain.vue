<script>
import PokemonCard from "./PokemonCard.vue";
import { store } from "../../src/data/store.js"
export default {
  name: "AppMain",
  data: () => ({ store }),
  components: { PokemonCard },
}
</script>

<template>
  <div class="container bg-danger">
    <div v-for="pokemon in store.pokemons" :key="pokemon.id"
      class="row row-cols-5 p-5 d-flex justify-content-between flex-wrap g-5">
      <div class="col p-2">
        <PokemonCard :pokemonData="pokemon" />
      </div>
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
