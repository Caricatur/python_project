<script setup>
import Header from "../components/Header.vue"
import Filter from "../components/Filter.vue"
import Map from "../components/Map.vue"
</script>

<template>
  <Header />
  <Filter />
  <Map />
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}
</style>
