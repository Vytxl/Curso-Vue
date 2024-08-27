<template>
 <div>
    <h2>Lista de Tareas</h2>
    <input type="text" v-model="nuevatarea" @keyup.enter="addTarea">
    <ul>
        <li v-for="(tarea , index) in tareas" :key="index">
            {{ tarea }}
            <button @click="borrarTarea">Borrar</button>

        </li>
    </ul>
 </div>
</template>

<script setup>
import {ref} from 'vue'
const tareas = ref([]);
const nuevatarea = ref('');
const addTarea = () =>{
    tareas.value.push(nuevatarea.value);
    nuevatarea.value = '';
}

const borrarTarea = (index) => {
    tareas.value.splice(index, 1);
}
</script>

<style scoped>

</style>