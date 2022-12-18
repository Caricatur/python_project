<template>
  <div class="map">
    <div id="map" class="h-full z-[1]"></div>
  </div>
</template>

<style scoped>
.map {
    background-color: #ffd670;
    grid-area: map;
    padding: 0;
    z-index: 1;
}

#map { 
  height: 100%; 
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

<script>
import leaflet from "leaflet"
import { onMounted } from "vue";
export default {
  name: "Map",
  components: {},
  setup() {
    let map;
    onMounted(() => {
      map = leaflet.map('map').setView([55.751244, 37.618423], 12);
      leaflet
        .tileLayer(
          `https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token=pk.eyJ1IjoiYW50eWF0cyIsImEiOiJjbGJ0aXBrZjExN2owM3dzM2d0bHJ1NWdrIn0.tU-T3OQH31H4s4dE_BL5lQ`,
          {
            maxZoom: 18,
            id: "mapbox/streets-v11", 
            style: "mapbox://styles/antyats/clbtj28pc004s14o9vpuncr4r",
            tileSize: 512,
            zoomOffset: -1,
            accessToken: "pk.eyJ1IjoiYW50eWF0cyIsImEiOiJjbGJ0aXBrZjExN2owM3dzM2d0bHJ1NWdrIn0.tU-T3OQH31H4s4dE_BL5lQ",
          }
        )
        .addTo(map);
    })
  }
}
</script>