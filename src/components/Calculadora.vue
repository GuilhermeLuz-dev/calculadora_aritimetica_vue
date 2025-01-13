<script setup>
const props = defineProps(['signal'])
</script>
<template>
    <div class="calculadora">
        <input type="number" id="firstNumber">
        <span id="signal">
            {{ props.signal }}
        </span>
        <input type="number" id="secundNumber">
        <span id="equals">=</span>
        <div id="result"></div>
    </div>
</template>
<style scoped>
#result {
    width: 50px;
    height: 5%;
    background-color: #fff;
}
</style>