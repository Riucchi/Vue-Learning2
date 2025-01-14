<script setup>
import {ref} from 'vue';
const hover = ref(true);
</script>
<template>
    <button @mouseenter="$event => hover = true" @mouseleave="hover = false"><slot name="icon" :hover="hover">😺</slot><slot>Click me!</slot></button>
    {{ hover }}
</template>
<style scoped>
button {
    background-color: #f1c40f;
    color: #fff;
    border: none;
    padding: 10px 20px;
    margin-bottom: 10px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1.2rem;
    transition: background-color 0.3s;
}
</style>