<template> <!-- Este es el template principal de la aplicación. Aquí se define la estructura y el contenido que se mostrará en la interfaz de usuario. -->
<MainView /> <!-- Este es el componente "MainView" que se ha importado anteriormente. Se renderiza aquí, lo que significa que su contenido y funcionalidad se integrarán en la aplicación principal. -->

</template>

<script setup> // logicalmente, el script setup es una forma de escribir componentes en Vue 3 que permite una sintaxis más concisa y fácil de entender. En este caso, no se necesita lógica adicional, pero se deja el bloque para futuras implementaciones.
import Contador from './components/Contador.vue'; // Importación del componente "Contador" que se encuentra en la carpeta "components". Este componente se utilizará dentro de la plantilla principal de la aplicación.
import ListaDeTareas from './components/ListaDeTareas.vue';
import MainView from './views/MainView.vue';
</script>


<style scoped> /* Estilos específicos para este componente. El uso de "scoped" asegura que estos estilos no afecten a otros componentes de la aplicación. */


</style>
