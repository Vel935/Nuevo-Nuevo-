<template>
    <div>
      <h2>Iniciar Sesión</h2>
      <form @submit.prevent="login">
        <label for="username">Nombre de usuario:</label>
        <input type="text" id="username" v-model="username" required>
        <br>
        <label for="password">Contraseña:</label>
        <input type="password" id="password" v-model="password" required>
        <br>
        <NuxtLink to="/tareas">
        <button type="submit">Iniciar Sesión</button>
      </NuxtLink>
        
      </form>
      <p v-if="error" class="error">{{ error }}</p>
      <p v-if="loggedIn" class="success">¡Has iniciado sesión correctamente!</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: '',
        password: '',
        error: '',
        loggedIn: false
      };
    },
    methods: {
      login() {
        // En un escenario real, aquí se realizaría la autenticación en el servidor.
        // Por simplicidad, verificamos si ambos campos están llenos.
  
        if (this.username === '' || this.password === '') {
          this.error = 'Por favor, completa ambos campos.';
          return;
        }
  
        // Suponemos que la autenticación es exitosa si los campos no están vacíos.
        this.error = '';
        this.loggedIn = true;
      }
    }
  };
  </script>
  
  <style scoped>
  /* Estilos CSS específicos para este componente, si es necesario */
  </style>
  