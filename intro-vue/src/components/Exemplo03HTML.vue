<script setup>
let text ='<p style="color:red"> Testando a diretiva v-html </p>'

</script>

<template>
	<div v-html="text"></div>
    <div>{{ text }}</div>
</template>