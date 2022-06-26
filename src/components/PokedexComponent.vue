<template>
  <div class="pokedex-component h-full p-8">
    <h1>CONTENTS</h1>
    <div v-for="e in list" class="pokemon">
      <div>{{ e.id }}</div>
      <div class="ml-12">{{ e.name }}</div>
    </div>
    <!-- <div class="flex justify-center">
      <h1>WELCOME TO POKéDEX</h1>
    </div>
    <div class="grid grid-cols-2 gap-4 pt-12">
      <div class="flex justify-center">
        <img
          class="w-24"
          src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/versions/generation-v/black-white/animated/1.gif"
        />
      </div>
      <div class="row-span-2">
        <div>BULBASAUR</div>
        <div>IVYSAUR</div>
        <div>VENUSAUR</div>
      </div>
      <div>09</div>
    </div> -->
  </div>
</template>

<script setup>
const list = [
  {
    id: "001",
    name: "BULBASAUR",
  },
  {
    id: "002",
    name: "IVYSAUR",
  },
  {
    id: "003",
    name: "VENUSAUR",
  },
  {
    id: "004",
    name: "CHARMENDER",
  },
  {
    id: "005",
    name: "CHARMELEON",
  },
  {
    id: "006",
    name: "CHARIZARD",
  },
  {
    id: "007",
    name: "SQUIRTLE",
  },
];
</script>

<style  scoped>
.pokedex-component {
  background-color: #fcf8fc;
}
</style>