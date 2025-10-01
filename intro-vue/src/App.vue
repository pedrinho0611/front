<script setup>
import { ref } from 'vue'
import ProductItem from './components/Avaliation/somativa/carrinho.vue'
// Array de produtos
let products = [
{ id: 1, name: 'Notebook', price: 3000 },
{ id: 2, name: 'Mouse'
, price: 50 },
{ id: 3, name: 'Teclado'
, price: 200 }
]
// Contador do carrinho
let cartCount = ref(0) 
// Função para adicionar ao carrinho
function handleAddToCart() {
    cartCount.value++
    emit('addToCart', cartCount.value)
}
</script>
<template>
<div class="app"></div>
<h1>Loja Virtual</h1>
 Contador de itens
<div class=
"cart-info">
<p>🛒 Itens no carrinho: {{ cartCount }}</p>
</div>
 Lista de produtos 
<div class="products-grid">
<ProductItem
v-for="product in products"
:key="product.id"
:name="product.name"
:price="product.price"
@addToCart="handleAddToCart"
/>
</div>
</template>