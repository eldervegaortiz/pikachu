<script setup>
import {ref} from 'vue';
const number=1;
let number2 = "hola mundo";

console.log(number)
console.log(number2.value)
</script>

<template>
 <h1 class="color-tittle">hello world</h1>
 <h1 class="color-tittle">{{ number }}</h1>
 <h1 class="color-tittle">{{ number2.toUpperCase() }}</h1>
  <h1 class="color-tittle">{{ number2.toLowerCase() }}</h1>

</template>




<style lang="css">
.color-tittle{
  background-color: blanchedalmond;
  text-align: center;
  color: blueviolet;
}
</style>
