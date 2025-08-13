<script setup>
let listas = ['pão','leite','Ovos','Frutas']

</script>

<template>
	<ul>
		<li v-for="(lista, index) in listas" >{{index + 1}}.{{ lista }}</li>
	</ul>
</template>

<style scoped>
ul {
	list-style-type: none;
	padding: 0;
}
</style>