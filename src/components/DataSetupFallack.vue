<script setup lang="ts">
import { result } from '../data.js'
import { ref } from 'vue';

const pokemons = ref( result )





</script>
<template >
  <div>

    <div v-for="pokemon in pokemons" :key="pokemon.i">
        {{ pokemon.name }} - <a :href="`${pokemon.url}`"> pokeapi link</a>
    </div>

  </div>
</template>