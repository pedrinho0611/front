<script setup>
let num1 =15
let num2 =25
</script>

<template>
    <p>{{ `A soma de ${num1} e ${num2} é: ${num1 + num2}` }}</p>
    <p>{{ `A subtração de ${num1} e ${num2} é: ${num1 - num2}` }}</p>
    <p>{{ `A multiplicação de ${num1} e ${num2} é: ${num1 * num2}` }}</p>
    <p>{{ `A divisão de ${num1} e ${num2} é: ${num1 / num2}` }}</p>
</template>