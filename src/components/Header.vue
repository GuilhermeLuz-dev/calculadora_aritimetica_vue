<script setup>
const props = defineProps(['editarOperator'])
</script>
<template>
    <header>
        <h1>Calculadora Aritimética</h1>
        <p>Escolha uma operação aritimética:</p>
        <select @change="props.editarOperator">
            <option selected value="soma">Soma</option>
            <option value="diferenca">Diferença</option>
            <option value="multiplicacao">Multiplicação</option>
            <option value="divisao">Divisão</option>
        </select>
    </header>
</template>
<style scoped>
select {
    color: black;
}
</style>