<script setup>
import {ref} from 'vue';
import tarjetasaludo from './components/tarjetasaludo.vue';

const contador = ref(0);
function incrementar(){
  contador.value++
}
</script>

<template>
 <h1>Mi primera APP</h1>
 <tarjetasaludo/>
  <tarjetasaludo/>
   <tarjetasaludo/>

<p>el numero es {{ contador }}</p>
<button @click="incrementar">+1</button>
<button @click="contador = 0">reset</button>
</template>




<style lang="css">


</style>
