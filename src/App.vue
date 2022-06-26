<script setup>
import { ref } from "vue";
import PokedexComponent from "./components/PokedexComponent.vue";
import PokemonMenu from "./components/PokemonMenu.vue";
const selectedView = ref(null);
</script>

<template>
  <div class="min-h-screen w-full console">
    <div class="game-boy-box">
      <template v-if="selectedView === null">
        <div class="grid grid-cols-2">
          <div class="col-start-2">
            <PokemonMenu @update="(e) => (selectedView = e)" />
          </div>
        </div>
      </template>
      <template v-else>
        <PokedexComponent class="col-span-3" />
      </template>
    </div>
  </div>
</template>

<style>
.console {
  background-image: url("https://raw.githubusercontent.com/TotallyGeeked/overlays/master/1920x1080/Game%20Boy/Game%20Boy%204x4%20(640x576).png");
  background-position: center;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
}
.game-boy-box {
  background-image: url("https://static.fandomspot.com/images/03/13219/05-pokemon-tower-area-screenshot-yellow.jpg");
  background-color: red;
  width: 640px;
  height: 576px;
}
</style>