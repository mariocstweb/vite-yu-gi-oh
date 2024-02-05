<script>
import { store } from "../data/store.js"
export default {
  name: "PokemonCard",
  props: {
    pokemonData: {
      type: Object,
      required: true,
    },
  },
};

</script>

<template>
  <div class="card">
    <img :src="pokemonData.imageUrl" class="img-fluid card-img-top img-container" alt="...">

    <div class="card-body text-center">
      <p class="card-text">{{ pokemonData.number }}</p>
      <h5 class="card-title">{{ pokemonData.name }}</h5>
      <p class="card-text">{{ pokemonData.type1 }}</p>
    </div>
  </div>
</template>


<style scoped>
.img-container {
  height: 200px;
  width: auto;

}
</style>
