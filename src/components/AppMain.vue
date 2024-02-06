<script>
import AppHeader from './AppHeader.vue';
import PokemonCard from "./PokemonCard.vue";
import SelectType from "./SelectType.vue";
import { store } from "../../src/data/store.js"
export default {
  name: "AppMain",
  data: () => ({
    store,
    filteredPokemons: [],

  }),
  components: { PokemonCard, SelectType },
  methods: {
    handleFilter(type) {
      if (type === "All") {
        this.filteredPokemons = this.store.pokemons;
      } else {
        this.filteredPokemons = this.store.pokemons.filter(
          (pokemon) => pokemon.type1 === type
        );
      }
    },
  },
};


</script>

<template>
  <main>
    <AppHeader @filter-by-type="handleFilter" />
    <div class="container">
      <div class="row row-cols-5 p-3 d-flex justify-content-between flex-wrap g-5">
        <!-- <div v-for="pokemon in store.pokemons" :key="pokemon._id" class="col p-3">
          <PokemonCard :pokemonData="pokemon" />
        </div> -->
        <div v-for="pokemon in filteredPokemons" :key="pokemon._id" class="col p-3">
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
