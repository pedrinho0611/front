<template>
	<div>
		<p v-if="idade >= 0 && idade <= 12">Criança</p>
		<p v-else-if="idade >= 13 && idade <= 17">Adolescente</p>
		<p v-else-if="idade >= 18 && idade <= 59">Adulto</p>
		<p v-else>Idoso</p>
	</div>
</template>

<script>
export default {
	data() {
		return {
			idade: 20
		}
	}
}
</script>
