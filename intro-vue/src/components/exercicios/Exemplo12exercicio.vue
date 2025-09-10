<template>
  <button class="button">
    <slot></slot>
  </button>
</template>

<script setup>
// Nenhuma lógica extra necessária para slot simples
</script>

<style scoped>
.button {
  padding: 10px 24px;
  font-size: 1rem;
  border-radius: 6px;
  border: none;
  background: #1976d2;
  color: #fff;
  cursor: pointer;
  transition: background 0.2s;
}
.button:hover {
  background: #1565c0;
}
</style>
