<template>
	<div>
		<p v-if="usuarioLogado">Bem-vindo</p>
		<p v-else>Faça login</p>
		<button @click="alternarLogin">
			{{ usuarioLogado ? 'Logout' : 'Login' }}
		</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			usuarioLogado: false
		}
	},
	methods: {
		alternarLogin() {
			this.usuarioLogado = !this.usuarioLogado;
		}
	}
}
</script>
