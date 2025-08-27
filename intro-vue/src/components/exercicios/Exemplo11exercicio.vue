<script setup>

import { computed } from 'vue'
const props = defineProps({
    titulo: String,
    preco: Number,
    imagem: {
        type: String,
        default: 'https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=100&q=80'
    },
    inStock: Boolean,
})

const statusClasse = computed(() => props.inStock ? 'ativo' : 'inativo')
const statusTexto = computed(() => props.inStock ? 'Disponível' : 'Indisponível')
function formatarPreco(valor) {
    return `R$ ${Number(valor).toFixed(2).replace('.', ',')}`
}

</script>

<template>
    <div class="card">
        <h3>{{ props.titulo }}</h3>
        <img v-if="props.imagem" :src="props.imagem" :alt="props.titulo" style="max-width:100px; margin-bottom:8px;" />
        <p><strong>Preço:</strong> {{ formatarPreco(props.preco) }}</p>
        <div :class="statusClasse">{{ statusTexto }}</div>
    </div>

</template>

<style scoped>
.card {
    border: 1px solid #ccc;
    padding: 1rem;
    margin: 1rem;
}

.ativo {
    color: green;
}

.inativo {
    color: red;
}
</style>