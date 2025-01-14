<script setup>
const props = defineProps(['signal', 'setNum', 'calcResult', 'firstNum', 'secundNum'])


</script>
<template>
    <div class="calculadora">
        <input :value="props.firstNum" @input="props.setNum" type="number" id="firstNumber">
        <span id="signal">
            {{ props.signal }}
        </span>
        <input :value="props.secundNum" @input="props.setNum" type="number" id="secundNumber">
        <span id="equals">=</span>
        <span id="result">
            {{ props.calcResult }}
        </span>
    </div>
</template>
<style scoped>
input {
    color: black;
    padding: 10px;
}

#result {
    padding: 10px;
    color: black;
    width: 50px;
    height: 50px;
    background-color: #fff;
}
</style>