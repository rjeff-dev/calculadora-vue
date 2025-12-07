<script setup>
import { reactive } from 'vue';

const calcularota  = reactive({

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
                    <input type="number" class="form-control">
                </div>
                <div class="col-5">
                    <label class="form-label" for="">Digite o segundo número:</label>
                    <input type="number" class="form-control">
                </div>
            </div>
            <form>
                <div class="row">
                    <div :class="['col-6', 'mt-5', 'd-flex', 'justify-content-center']">
                        <button type="button" class="btn btn-primary">Soma +</button>
                    </div>
                    <div :class="['col-6', 'mt-5', 'd-flex', 'justify-content-center']">
                        <button type="button" class="btn btn-primary">Divisão ÷</button>
                    </div>
                    <div :class="['col-6', 'mt-5', 'd-flex', 'justify-content-center']">
                        <button type="button" class="btn btn-primary">Subtração -</button>
                    </div>
                    <div :class="['col-6', 'mt-5', 'd-flex', 'justify-content-center']">
                        <button type="button" class="btn btn-primary">Multplicação ×</button>
                    </div>
                </div>
                <div class="row">
                    <div :class="['col', 'mt-5', 'd-flex', 'justify-content-center']">
                        <button type="button" :class="['btn', 'btn-success']">Calcular</button>
                    </div>
                </div>
            </form>

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
</style>
