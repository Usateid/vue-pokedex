<script setup>
import { ref } from "vue";
import PokedexComponent from "./components/PokedexComponent.vue";
import PokemonMenu from "./components/PokemonMenu.vue";

const selection = ref(null);
</script>

<template>
  <div class="bg-slate-100 container mx-auto">
    <div class="min-h-screen grid grid-cols-3 gap-8 py-16">
      <PokemonMenu class="" @update="(e) => (selection = e)" />
      <PokedexComponent class="col-span-2" />
    </div>
  </div>
</template>

<style>
</style>
