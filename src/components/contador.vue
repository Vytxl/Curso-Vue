<template>
<h1>Hello World</h1>
<p>{{ contador }}</p>
<button @click="incrementar">Incrementar</button>
<button @click="decrementar">Decrementar</button>
</template>

<script setup>
//Importamos ref para crear variables reactivas
import {ref} from 'vue';

//creamos unas constante llamada contador
const contador = ref(0);

//Funcion para incrementar
const incrementar = () =>{
  contador.value++
}
//Funcion para decrementar
const decrementar = () =>{
  contador.value--
}
</script>

<style scoped>
p {
  color: red;
  }
</style>

