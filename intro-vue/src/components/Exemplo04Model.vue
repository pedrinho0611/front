<script selut>
    import {ref} from 'vue'
    let texto = ref('')
</script>

<template>
    <p> valor do input: {{ texto }}</p>
    <input type="text" v-model="texto" >
</template>