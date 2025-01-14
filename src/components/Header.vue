<script setup>
const props = defineProps(['setOperator'])
</script>
<template>
    <header>
        <h1 class="title">Calculadora Aritimética</h1>
        <div class="select">
            <p>Escolha uma operação aritimética:</p>
            <select class="select_operator" @change="props.setOperator">
                <option selected value="+">Adição</option>
                <option value="-">Subtração</option>
                <option value="*">Multiplicação</option>
                <option value="/">Divisão</option>
            </select>
        </div>
    </header>
</template>
<style scoped>
.title {
    text-align: center;
    padding-top: 50px;
    margin-bottom: 50px;
    font-size: 48px;
    font-weight: bold;
    background: linear-gradient(90deg, #579FD4, #33D88E);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.select {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
}

.select p {
    font-size: 25px;
}

.select_operator {
    padding: 10px;
    color: #fff;
    margin-left: 10px;
    font-weight: bold;
    font-size: 20px;
    background-color: #0695fc;
    border: none;
    border-radius: 10px;
}
</style>