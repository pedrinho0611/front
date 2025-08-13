<script setup>
import { ref, computed } from 'vue';

const peso = ref('');
const altura = ref('');

const imc = computed(() => {
    const p = parseFloat(peso.value);
    const a = parseFloat(altura.value);
    if (!p || !a) return '';
    return (p / (a * a)).toFixed(2);
});

const classificacao = computed(() => {
    const valor = parseFloat(imc.value);
    if (!valor) return '';
    if (valor < 18.5) return 'Abaixo do peso';
    if (valor < 25) return 'Peso normal';
    if (valor < 30) return 'Sobrepeso';
    if (valor < 35) return 'Obesidade grau I';
    if (valor < 40) return 'Obesidade grau II';
    return 'Obesidade grau III';
});
</script>

<template>
    <div>
        <h1>Cálculo de IMC</h1>
        <label>Peso (kg): <input type="number" v-model="peso" step="0.01" /></label><br />
        <label>Altura (m): <input type="number" v-model="altura" step="0.01" /></label><br />
        <p v-if="imc">IMC: {{ imc }}</p>
        <p v-if="classificacao">Classificação: {{ classificacao }}</p>
    </div>
</template>
