<template>
<div class="sidebar">
    <h2>Barra lateral</h2>
    <ul>
    <li><router-link to="/contador"> Contador </router-link></li>
    <li><router-link to="/listaDeTareas"> Lista de tareas  </router-link></li>
    </ul>
</div>
</template>

<script setup>

</script>

<style>
.sidebar {
 width: 20px0px; /* Ancho de la barra lateral */;
 background-color: rgb(225, 225, 235); /* Color de fondo de la barra lateral */
 padding: 20 px; /* Espacio interno alrededor del contenido de la barra lateral */
}
</style>