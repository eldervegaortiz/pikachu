<script setup>
const nombre= "Joan Esteban Buitrago"
const telefono= 31035698
const ciudad = "socorro"
const edad = 19


</script>


<template>
<div class="contenedor-tarjeta">
<h2>{{ nombre }}</h2>
<h3>Telefono:{{ telefono }}</h3>
<h3>Ciudad:{{ ciudad }}</h3>
<h3>Edad:{{ edad }}</h3>
<p v-if="edad>18">es mayor de edad</p>
</div>
</template>

<style lang="css">
.contenedor-tarjeta{
    display: block;
    margin: 20px,auto;
    text-align: center;
    align-items: center;
    
}
</style>