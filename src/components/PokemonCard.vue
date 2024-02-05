<script>
import { store } from "../../src/data/store.js"
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
    <img :src="pokemonData.imageUrl" class="card-img-top" alt="...">
    <div class="card-body">
      <p class="card-text"></p>
      <h5 class="card-title">Card title</h5>
      <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
        content.</p>
    </div>
  </div>
</template>


<style scoped></style>
