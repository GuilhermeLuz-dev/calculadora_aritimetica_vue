<script setup>
import { reactive } from 'vue';
import Header from './components/Header.vue';
import Calculadora from './components/Calculadora.vue';

const state = reactive({
  operator: 'soma'
})

function getOperator() {
  switch (state.operator) {
    case 'soma':
      return '+'
    case 'diferenca':
      return '-'
    case 'multiplicacao':
      return 'X'
    default:
      return '/'
  }
}
</script>
<template>
  <div class="background">
    <div class="container">
      <Header :editarOperator="event => state.operator = event.target.value"></Header>
      <Calculadora :signal="getOperator()"></Calculadora>
    </div>
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  color: #fff;
}

.background {
  width: 100%;
  height: 100vh;
  background-color: #000;
}

.container {
  width: 100%;
  max-width: 674px;
  display: block;
  margin: 0 auto;
}
</style>
