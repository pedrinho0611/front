<script setup>
const dataAtual = new Date();
</script>

<template>
  <div>
    <p>Data atual:</p>
    <p>
      Ano: {{ dataAtual.getFullYear() }}<br>
      Mês: {{ dataAtual.getMonth() + 1 }}<br>
      Dia: {{ dataAtual.getDate() }}
    </p>
  </div>
</template>