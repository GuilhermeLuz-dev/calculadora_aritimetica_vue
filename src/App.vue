<script setup>
import { reactive } from 'vue';
import Header from './components/Header.vue';
import Calculadora from './components/Calculadora.vue';
import Footer from './components/Footer.vue';

const state = reactive({
  operator: '+',
  firstNum: 0,
  secundNum: 0,
  result: 0
})

const editOperator = event => {
  state.operator = event.target.value
  state.result = calculate();
};

const setNumbers = (e) => {
  if (e.target.id === "firstNumber") {
    state.firstNum = e.target.value;
  } else {
    state.secundNum = e.target.value;
  }
  state.result = calculate();
};

const calculate = () => {
  let { operator, firstNum, secundNum } = state;
  firstNum = Number(firstNum);
  secundNum = Number(secundNum);
  switch (operator) {
    case '+':
      return firstNum + secundNum;
    case '-':
      return firstNum - secundNum;
    case '*':
      return firstNum * secundNum;
    case '/':
      return firstNum / secundNum;
    default:
      alert("Ocorreu um erro com o operador escolhido");
      break
  }
}
</script>
<template>
  <div class="background">
    <div class="container">
      <Header :setOperator="editOperator"></Header>
      <Calculadora :signal="state.operator" :setNum="setNumbers" :calcResult="state.result" :firstNum="state.firstNum"
        :secundNum="state.secundNum"></Calculadora>
      <Footer></Footer>
    </div>
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  color: #fff;
  font-family: 'Source Sans Pro', Arial, Helvetica, sans-serif;
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
