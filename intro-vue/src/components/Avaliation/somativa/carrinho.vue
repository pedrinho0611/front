<script setup>
import { defineProps, defineEmits } from 'vue'
// Declaração das props
const props = defineProps({
name: String,
price: Number
})
// Declaração dos emits
const emit = defineEmits(['addToCart'])
// Função para adicionar ao carrinho
function adicionarAoCarrinho() {
emit('addToCart')
}
</script>
<template>
<div class="product-card">
<h3>{{ props.name }}</h3>
<p class="price">R$ {{ props.price }}</p>
<button @click="adicionarAoCarrinho()" class="btn-add" >
Adicionar ao Carrinho
</button>
</div>
</template>