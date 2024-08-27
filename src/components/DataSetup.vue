<script setup lang="ts">
import axios from 'axios'
import { ref } from 'vue';

const pokemons = ref([])
const { data } = await axios.get('https://pokeapi.co/api/v2/pokemon?limit=100000&offset=0').catch((error) => {
  alert(error)
})

pokemons.value = data.results

</script>
<template >
  <div>

    <div v-for="pokemon in pokemons" :key="pokemon.i">
        {{ pokemon.name }} - <a :href="`${pokemon.url}`"> pokeapi link</a>
    </div>

  </div>
</template>