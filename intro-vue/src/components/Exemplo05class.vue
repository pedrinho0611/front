<script setup>
let vaidacao = false
let isError = false
let isActive = true
let isDisable = false
</script>

<template>

    <p :class="{
    'ok': isActive,
    'falha': isError
    }">teste de diretiva Class</p>

    <button :disabled="isDisable">Clique aqui</button>

</template>

<style scoped>
.ok {
    color: green;
}
.falha {
    color: red;
}
</style>