<template>
  <card :titulo="titulo" :descricao="descricao">
    <template #default>
      <slot></slot>
    </template>
    <template #footer>
      <slot name="footer"></slot>
    </template>
  </card>
</template>

<script setup>
import card from './card.vue'
const props = defineProps({
  titulo: {
    type: String,
    required: true
  },
  descricao: {
    type: String,
    required: true
  }
})
</script>
