<script setup>
</script>

<template>
  <div class="map">
    <h1 class="test">map</h1>
  </div>
</template>

<style scoped>
.map {
    background-color: #ffd670;
    grid-area: map;
    padding: 0;
    display: flex;
    justify-content: center;
    align-content: center;
    flex-direction: column;
}
.test {
    text-align: center;
    color: white;
}

@media screen and (max-width:420px) {
    .map {
        display: none;
    }
}

</style>
