<script>
export default {
  name: "SelectType",
  data: () => ({
    types: ["Bug", "Dark", "Dragon", "Electric", "Fairy", "Fighting", "Fire", "Flying", "Ghost", "Grass", "Ground", "Ice", "Normal", "Poison", "Psychic", "Rock", "Steel", "Water"]
  })
}
</script>


<template>
  <select class="form-select" aria-label="Default select example">
    <option selected>All</option>
    <option v-for="type in types" :key="type" :value="type">{{ type }}</option>
  </select>
</template>

<style scoped>
select {
  width: 15%;
}
</style>