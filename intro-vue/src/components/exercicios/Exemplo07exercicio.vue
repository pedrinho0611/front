<script setup>
const produtos = [
	{ nome: 'Notebook', preco: 3500, categoria: 'Eletrônicos' },
	{ nome: 'Camiseta', preco: 50, categoria: 'Vestuário' },
	{ nome: 'Café', preco: 18.5, categoria: 'Alimentos' },
	{ nome: 'Livro', preco: 42.9, categoria: 'Educação' }
]

function formatarPreco(valor) {
	return `R$ ${valor.toFixed(2).replace('.', ',')}`
}
</script>

<template>
	<div class="produtos">
		<div class="card" v-for="(produto, index) in produtos" :key="index">
			<h3>{{ produto.nome }}</h3>
			<p><strong>Preço:</strong> {{ formatarPreco(produto.preco) }}</p>
			<p><strong>Categoria:</strong> {{ produto.categoria }}</p>
		</div>
	</div>
</template>

<style scoped>
.produtos {
	display: flex;
	flex-wrap: wrap;
	gap: 16px;
}
.card {
	border: 1px solid #ccc;
	border-radius: 8px;
	padding: 16px;
	width: 200px;
	box-shadow: 2px 2px 8px rgba(0,0,0,0.05);
}
.card h3 {
	margin: 0 0 8px 0;
}
</style>