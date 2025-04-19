<template> <!-- Este es el template principal de la aplicación. Aquí se define la estructura y el contenido que se mostrará en la interfaz de usuario. -->
  <h1>🤣 HOLA MUNDO DESDE VUE</h1>
  <p>{{ contador }}</p> <!-- Esta es una interpolación de Vue que mostrará el valor de la variable "contador" en la interfaz de usuario. -->
  <button @click="incrementar">INCREMENTAR</button>
  <button @click="decrementar">DECREMENTAR</button>
</template>

<script setup> // logicalmente, el script setup es una forma de escribir componentes en Vue 3 que permite una sintaxis más concisa y fácil de entender. En este caso, no se necesita lógica adicional, pero se deja el bloque para futuras implementaciones.
import { ref } from "vue"; // Importaciones de Vue. En este caso, no se están utilizando, pero se deja el bloque para futuras implementaciones.
const contador = ref(0); // Definición de una variable reactiva llamada "contador" que se inicializa en 0. Esta variable puede ser utilizada para llevar un conteo o cualquier otra lógica que requiera reactividad.
const incrementar = ( ) => { // Definición de una función llamada "incrementar" que incrementa el valor de "contador" en 1 cada vez que se llama. Esta función se puede vincular a un evento, como un clic en un botón.
  contador.value++;
}; // Fin de la función "incrementar".
const decrementar = ( ) => { // Definición de una función llamada "decrementar" que decrementa el valor de "contador" en 1 cada vez que se llama. Esta función se puede vincular a un evento, como un clic en un botón.
  contador.value--;
}; // Fin de la función "decrementar".
</script>


<style scoped> /* Estilos específicos para este componente. El uso de "scoped" asegura que estos estilos no afecten a otros componentes de la aplicación. */
p {
  color: red;
}

</style>
