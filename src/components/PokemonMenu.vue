<template>
  <div>
    <ul class="framed buttons">
      <li v-for="element in optionsList">
        <button @click="selection = element">{{ element }}</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, watchEffect, defineEmits } from "vue";
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

<style lang="scss" scoped>
</style>