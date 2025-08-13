<script setup>
let nomes = ['Pedro', 'livia', 'augusto']
</script>

<template>
    
	<ul>
		<li v-for="nome in nomes" :key="nome">{{ nome }}</li>
	</ul>

</template>
