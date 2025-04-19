<template>
<div class="container">
    <Sidebar> </Sidebar> <!-- Este es el componente Sidebar que se ha importado anteriormente. Se renderiza aquí, lo que significa que su contenido y funcionalidad se integrarán en la aplicación principal. -->
    <div class="content">
        <router-view></router-view> <!-- Este es el componente "router-view" que se utiliza en Vue Router para renderizar los componentes de vista según la ruta actual. Es un espacio reservado donde se mostrarán los componentes correspondientes a las rutas definidas en la configuración del enrutador. -->
    </div>        
</div>
</template>

<script setup>
import Sidebar from '../components/Sidebar.vue'; // Importa el componente Sidebar para usarlo en la vista principal.


</script>

<style>
.container {
  display: flex; /* Utiliza flexbox para alinear los elementos dentro del contenedor. */
 /*flex-direction: column; /* Establece la dirección de los elementos secundarios en una columna. */ 
 /*justify-content: center; /* Centra los elementos secundarios verticalmente dentro del contenedor. */
 /*align-items: center; /* Centra los elementos secundarios horizontalmente dentro del contenedor. */
 /*height: 100vh;   /* Establece la altura del contenedor al 100% de la altura de la ventana del navegador. */  
 /*background-color: #f0f0f0; /* Establece un color de fondo claro para el contenedor. */ 
}

.content {
  /*background-color: #fff; /* Establece un color de fondo blanco para el contenido. */
  flex: 1;
  padding: 20px; /* Agrega un relleno interno de 20 píxeles alrededor del contenido. */
  /*border-radius: 8px; /* Redondea los bordes del contenido con un radio de 8 píxeles. */
  /*box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Agrega una sombra sutil al contenido para darle profundidad. */
}
</style>