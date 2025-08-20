<script setup>
import { ref } from 'vue'

const estado = ref('ativo') // 'ativo', 'inativo', 'carregando'

function setEstado(novoEstado) {
	estado.value = novoEstado
}
</script>

<template>
	<div class="botoes-container">
		<button
			:class="['botao', estado === 'ativo' ? 'ativo' : estado === 'inativo' ? 'inativo' : 'carregando']"
			:disabled="estado === 'inativo' || estado === 'carregando'"
		>
			<span v-if="estado === 'carregando'">Carregando...</span>
			<span v-else-if="estado === 'ativo'">Ativo</span>
			<span v-else>Inativo</span>
		</button>
		<div class="troca-estado">
			<button @click="setEstado('ativo')">Ativar</button>
			<button @click="setEstado('inativo')">Inativar</button>
			<button @click="setEstado('carregando')">Carregar</button>
		</div>
	</div>
</template>

<style scoped>
.botoes-container {
	display: flex;
	flex-direction: column;
	gap: 16px;
	align-items: flex-start;
}
.botao {
	padding: 10px 24px;
	font-size: 1rem;
	border-radius: 6px;
	border: none;
	transition: background 0.2s, color 0.2s;
}
.botao.ativo {
	background: #4caf50;
	color: #fff;
	box-shadow: 0 2px 8px rgba(76,175,80,0.15);
}
.botao.inativo {
	background: #bdbdbd;
	color: #666;
	cursor: not-allowed;
}
.botao.carregando {
	background: #2196f3;
	color: #fff;
	position: relative;
}
.troca-estado button {
	margin-right: 8px;
	padding: 6px 16px;
	border-radius: 4px;
	border: none;
	background: #eee;
	cursor: pointer;
	font-size: 0.95rem;
}
.troca-estado button:hover {
	background: #ddd;
}
</style>
