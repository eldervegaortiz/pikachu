<script setup>
import tarjetasaludo from './components/tarjetasaludo.vue';
import { getPokemon } from './api/pokeapi.js';
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount } from 'vue';

let loading = ref(true);
let pokemon = ref({});
let hora = ref('');
let intervalo = null;

onBeforeMount(() => {
  console.log('aun no hay dom');
});

onMounted(async () => {
  pokemon.value = await getPokemon('pikachu');
  console.log('pokemon .value');
  loading.value = false;

  hora.value = new Date().toLocaleTimeString();
  intervalo = setInterval(() => {
    hora.value = new Date().toLocaleTimeString();
  }, 1000);
});

onBeforeUpdate(() => {
  console.log('antes de actualizar');
});

onUpdated(() => {
  console.log('despues de actualizar');
});

onBeforeUnmount(() => {
  console.log('antes de desmontar');
  clearInterval(intervalo);
});
</script>

<template>
  <p v-if="loading">Cargando Datos</p>
  <div v-else>
    <h1>{{ pokemon?.name }}</h1>
    <img :src="pokemon?.sprites?.other?.home?.front_default" :alt="pokemon?.name" width="250" />
  </div>
  <p class="reloj">🟢 {{ hora }}</p>
</template>

<style>

</style>
