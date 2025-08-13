<script setup>
let nomes = ['Pedro', 'livia', 'augusto']
</script>

<template>

	<ul>
		<li v-for="(nome, index) in nomes" >{{index + 1}}.{{ nome }}</li>
	</ul>
</template>
    