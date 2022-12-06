<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld />
    </div>
  </header>
</template>

<style scoped>
.wrapper {
  display: grid;
  grid-template-areas: 
    "header header header"
    "data map map";
  grid-template-rows: 7rem 1fr;
  grid-template-columns: 50% 50%;  
  margin: 0;
  padding: 3px;
}

@media screen and (max-width:420px) {
    .wrapper {
      grid-template-areas: 
    "header header header"
    "data data data"
    "footer footer footer";
    }
}

</style>