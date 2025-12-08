<script setup>
import { computed, reactive } from 'vue';

const calc  = reactive({
    n1: '',
    n2: '',
    op: "soma",
})

//<=================================Funções para a calculadora=======================================>
const resultado = computed( () => {
    const n1 = Number(calc.n1);
    const n2 = Number(calc.n2);

    switch (calc.op) {
        case "soma":return n1 + n2;
        case "sub":return n1 - n2;
        case "mult":return n1 * n2;
        case "div": return n2 === 0 ?"Erro: Divisão por zero" : n1 / n2;
        default: return '';
    }
})
</script>

<template>
    <div class="pagina">
        <div class="container">
            <header :class="['p-5', 'mt-4', 'mb-4', 'header-bc', 'rounded-3', 'd-flex', 'justify-content-center', 'align-items-center','text-center']">
                <h1>Calculadora aritmética</h1>
            </header>
            <div class="d-flex justify-content-between">
                <div class="col-5">
                    <label class="form-label" for="">Digite o primeiro número:</label>
                    <input type="number" class="form-control" v-model="calc.n1">
                </div>
                <div class="col-5">
                    <label class="form-label" for="">Digite o segundo número:</label>
                    <input type="number" class="form-control" v-model="calc.n2">
                </div>
            </div>
            <div class="row mt-4">
                <div class="col-12">
                    <label for="form-label">Escolha a operação:</label>
                    <select class="form-select" v-model="calc.op">
                        <option value="soma">Somar (+)</option>
                        <option value="sub">Subtração (-)</option>
                        <option value="mult">Multiplicação (*)</option>
                        <option value="div">Divisão (÷)</option>
                    </select>
                </div>
            </div>
            <div class="row">
                <div class="col mt-5 d-flex justify-content-center">
                    <p class="operacao">
                        Resultado: {{ resultado }}
                    </p>
                </div>
            </div>

        </div>
    </div>
</template>

<style scoped>
    :global(html),
    :global(body) {
        margin: 0;
        padding: 0;
        background-color: rgb(26, 0, 51);
        height: 100%;
    }
    .pagina{
        background-color: rgb(26, 0, 51);
        min-height: 100vh;         
        width: 100%;               
        color: #00ffff;
    }
    .header-bc{
        background-color: #8c4ef7;
    }
    .operacao{
        font-size: 24px;
    }
</style>
