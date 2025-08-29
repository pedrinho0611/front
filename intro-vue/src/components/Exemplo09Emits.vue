<script setup>
import { ref} from 'vue'

const emit = defineEmits(['update'])
const count = ref(0)

function Incrementar() {
    count.value++
    emit('update', count.value)
}
</script>

<template>
    <div>
        <p> Contador:{{ count }}</p>
        <button @click="Incrementar">+1</button>
    </div>
</template>

<style scoped>
</style>