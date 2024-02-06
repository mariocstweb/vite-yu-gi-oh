<script>
import SelectType from "./SelectType.vue"
export default {
  name: "AppHeader",
  components: { SelectType },
}

</script>

<template>
  <header>
    <div class="d-flex justify-content-center">
      <img src="../../public/IMG_5941.png" alt="" class="mt-2">
    </div>

    <div class="container d-flex justify-content-between align-items-start h-100 pt-5 ps-0">
      <div class="d-flex">
        <div class="pokedex-big me-2"></div>
        <div class="pokedex pk-red me-2"></div>
        <div class="pokedex pk-y me-3"></div>
        <div class="pokedex pk-g me-3 "></div>
      </div>
      <SelectType @change="$emit('filter-by-type', $event.target.value)" />
    </div>
  </header>
</template>

<style scoped>
header {
  background-color: #B71B1B;
  min-height: 300px
}

.pokedex-big {
  border: 4px solid white;
  border-radius: 50%;
  height: 80px;
  width: 80px;
  background: rgb(255, 255, 255);
  background: linear-gradient(45deg, rgba(255, 255, 255, 1) 0%, rgba(16, 67, 255, 1) 58%);
}

.pokedex {
  border: 2px solid white;
  border-radius: 50%;
  height: 50px;
  width: 50px;
}

.pk-red {
  background: rgb(255, 255, 255);
  background: linear-gradient(45deg, rgba(255, 255, 255, 1) 0%, rgba(255, 16, 16, 1) 58%);
}

.pk-y {
  background: rgb(255, 255, 255);
  background: linear-gradient(45deg, rgba(255, 255, 255, 1) 0%, rgba(255, 234, 16, 1) 58%);
}

.pk-g {
  background: rgb(255, 255, 255);
  background: linear-gradient(45deg, rgba(255, 255, 255, 1) 0%, rgba(16, 255, 21, 1) 58%);
}

img {
  height: 100px;
}
</style>
