<script setup>
const props = defineProps(['setOperator'])
</script>
<template>
    <header>
        <h1>Calculadora Aritimética</h1>
        <p>Escolha uma operação aritimética:</p>
        <select @change="props.setOperator">
            <option selected value="+">Soma</option>
            <option value="-">Diferença</option>
            <option value="*">Multiplicação</option>
            <option value="/">Divisão</option>
        </select>
    </header>
</template>
<style scoped>
select {
    color: black;
}
</style>