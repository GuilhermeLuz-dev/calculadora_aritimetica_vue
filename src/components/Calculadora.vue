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
        <div id="result">
            {{ props.calcResult }}
        </div>
    </div>
</template>
<style scoped>
.calculadora {
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(90deg, #579FD4, 90%, #33D88E);
    padding: 30px;
    border-radius: 10px;
}

input,
#result {
    width: 70px;
    height: 40px;
    border-radius: 10px;
    border: none;
    color: black;
    padding: 10px;
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    font-weight: bold;
}

#signal,
#equals {
    margin: 0 30px;
    font-size: 40px;
    font-weight: bold;
}
</style>