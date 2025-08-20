<script setup>
let vaidacao = false
let isError = false
let isActive = true
</script>

<template>

    <p :class="{
    'ok': isActive,
    'falha': isError
    }">teste de diretiva Class</p>

</template>

<style scoped>
.ok {
    color: green;
}
.falha {
    color: red;
}
</style>