<template>
  <div class="pokemon-menu bg-white">
    <ul class="framed buttons">
      <li v-for="element in optionsList">
        <button @click="selection = element">{{ element }}</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, watchEffect } from "vue";
let selection = ref(null);
const emit = defineEmits(["update"]);

watchEffect(() => emit("update", selection.value));
const optionsList = [
  "Pokédex",
  "Pokémon",
  "Item",
  "Player",
  "Save",
  "Option",
  "Exit",
];
</script>

<style scoped>
.pokemon-menu {
  margin: 0 0 0 0;
}
</style>