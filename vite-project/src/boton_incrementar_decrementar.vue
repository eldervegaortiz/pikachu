<script setup>
import { ref } from 'vue'

const contador = ref(0)

function incrementar() {
  contador.value++
}

function decrementar() {
  contador.value--
}
</script>

<template>
  <p>
    El número es
    <span :class="contador < 0 ? 'rojo' : 'verde' ">
      {{ contador }}
    </span>
  </p>

  <button @click="decrementar" :disabled="contador <= -5">-1</button>
  <button @click="incrementar">+1</button>
  <button @click="contador = 0">Reset</button>
</template>

<style>
.rojo {
  color: red;
}

.verde {
  color: green;
}

button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
</style>
