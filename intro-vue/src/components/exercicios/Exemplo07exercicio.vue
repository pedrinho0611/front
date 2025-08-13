<script setup>
const produtos = [
    { nome: 'Notebook', preco: 3500, categoria: 'Eletrônicos' },
    { nome: 'Camiseta', preco: 50, categoria: 'Vestuário' },
    { nome: 'Café', preco: 18.5, categoria: 'Alimentos' },
    { nome: 'Livro', preco: 42.9, categoria: 'Educação' }
]

</script>

<template>
    <div v-for="produto in produtos">
        <h3>{{ produto.nome }}</h3>
        <p><strong>Preço:</strong> R$ {{ produto.preco.toFixed(2).replace('.', ',') }}</p>
        <p><strong>Categoria:</strong> {{ produto.categoria }}</p>
    </div>


	
</template>

<style scoped>
.card{
    border: 1px solid white;
    border-radius: 5px;
    padding: 10px;
    margin-bottom: 10px;
}
</style>