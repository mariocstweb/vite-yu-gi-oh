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
  <main>
    <div class="container">
      <div class="row row-cols-5 p-3 d-flex justify-content-between flex-wrap g-5">
        <div v-for="pokemon in store.pokemons" :key="pokemon._id" class="col p-3">
          <PokemonCard :pokemonData="pokemon" />
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
.row {

  background-color: #DEDEDE;
  border-radius: 30px;
}

main {
  background-color: #B71B1B;
}
</style>
