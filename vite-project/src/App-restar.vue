<script setup>
import {ref} from 'vue';
import tarjetasaludo from './components/tarjetasaludo.vue';

const numero1 = 5;
const numero2 = 8;
let resultado = ref(0);

function sumar(){
resultado.value = numero1 + numero2
  
}
function restar(){
 resultado.value = numero1 - numero2
}


let edad = ref(10);
</script>

<template>
 <h1>Mi primera APP</h1>
 <p>el resultado es {{ resultado }}</p>
<button @click="restar">restar</button>
<button @click="sumar">sumar</button>
<p v-if="edad>18">es mayor de edad</p>

<button @click="edad=19">19 años</button>
<button @click="edad=10">reset</button>
</template>




<style lang="css">


</style>
