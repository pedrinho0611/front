<script setup>
import { ref } from 'vue';
let nome = ref('');
let email = ref('');
let idade = ref('');
let bio = ref('');
</script>

<template>
    <div>
        <label>Nome: <input type="text" v-model="nome" /></label><br />
        <label>Email: <input type="email" v-model="email" /></label><br />
        <label>Idade: <input type="number" v-model="idade" /></label><br />
        <label>Bio: <textarea v-model="bio"></textarea></label>
        <p>Nome: {{ nome }}</p>
        <p>Email: {{ email }}</p>
        <p>Idade: {{ idade }}</p>
        <p>Bio: {{ bio }}</p>
    </div>
</template>