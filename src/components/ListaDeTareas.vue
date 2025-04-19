<template>
    <div>
        <h2>Lista de tareas</h2>
        <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea"/> <!-- Campo de entrada para agregar una nueva tarea. Utiliza la directiva v-model para enlazar el valor del campo con la referencia reactiva 'nuevaTarea'. -->
        <ul>
            <li v-for="(tarea, index) in tareas" :key="index"> <!-- Itera sobre el array de tareas y muestra cada tarea en una lista. 'v-for' se utiliza para crear una lista basada en el array 'tareas'. 'index' es el índice de la tarea actual en la iteración. -->
                {{ tarea }} <!-- Muestra el nombre de la tarea. -->
                 <button @click="borrarTarea"> Eliminar tarea</button>   
            </li>
        </ul>
    </div>
</template>
<script setup> 
import { ref } from 'vue'; // Importa la función 'ref' de Vue para crear referencias reactivas.
const tareas = ref([]); // Crea una referencia reactiva llamada 'tareas' que inicialmente es un array vacío.
const nuevaTarea = ref(''); // Crea una referencia reactiva llamada 'nuevaTarea' que inicialmente es una cadena vacía.
const addTarea = () =>{
    tareas.value.push(nuevaTarea.value); // Agrega la nueva tarea al array de tareas.
    nuevaTarea.value = ''; // Limpia el campo de entrada después de agregar la tarea.
}
const borrarTarea = (index) => {
    tareas.value.splice(index, 1); // Elimina la tarea en el índice especificado del array de tareas.
}
</script>
<style></style>