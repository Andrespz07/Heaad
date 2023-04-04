<script setup>
import { ref } from 'vue'
import cara from '../assets/cara.jpg'
import cruz from '../assets/cruz.jpg'

const moneda = ref('')

function lanzarMoneda() {
  const resultado = Math.random() < 0.5 ? cara : cruz
  moneda.value = resultado
}
</script>

<template>
  <div>
    <img v-if="moneda === cara" :src="moneda" alt="Moneda cara">
    <img v-else-if="moneda === cruz" :src="moneda" alt="Moneda cruz">
    <button @click="lanzarMoneda">Lanzar moneda</button>
  </div>
</template>

<style lang="scss" scoped>
  img {
    max-width: 200px;
    max-height: 200px;
  }
</style>
