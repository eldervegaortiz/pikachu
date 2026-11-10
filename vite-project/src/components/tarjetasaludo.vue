<script setup>
import {ref} from 'vue';
const message = "soy joan"
</script>

<template>
  <article class="tarjeta">
<h1>hola {{ message }}</h1>
  </article>


</template>




<style lang="css">
.tarjeta{
  background-color: rgb(18, 17, 15);
  border: 40px solid rgb(rgb(198, 135, 135));
  padding: 2rem;
  
}

</style>
