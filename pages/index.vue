<template>
  <div>
    <center>
      <h1>Bienvenidos a la app de tareas</h1>
      <p>Esta es una aplicación que permite gestionar las tareas de los estudiantes</p>

      <a href="/tareas">Click para iniciar (sin nuxtLink)</a>
<br>

<br>
      <Login/>
    
      
    </center>
    

  </div>
</template>
<script>

definePageMeta({
  layout: "blank",
});

import Login from "~/components/tasks/login.vue";
import Formulario from "~/components/tasks/login.vue";

export default {
  components: {
    Formulario,
    Login
},
  head: {
    title: 'Formulario de Ejemplo' // Puedes personalizar el título de la página aquí
  }
};


</script>