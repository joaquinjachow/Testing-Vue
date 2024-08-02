<template>
  <div>
    <form @submit.prevent="enviarFormulario">
      <div>
        <label for="nombre">Nombre:</label>
        <input type="text" v-model="form.nombre" id="nombre" required>
      </div>
      <div>
        <label for="apellido">Apellido:</label>
        <input type="text" v-model="form.apellido" id="apellido" required>
      </div>
      <div>
        <label for="email">Correo Electrónico:</label>
        <input type="email" v-model="form.email" id="email" required>
      </div>
      <div>
        <label for="password">Contraseña:</label>
        <input type="password" v-model="form.password" id="password" required>
      </div>
      <button type="submit">Enviar</button>
    </form>
  </div>
</template>

<script>

export default {
  data() {
    return {
      form: {
        nombre: '',
        apellido: '',
        email: '',
        password: ''
      }
    };
  },
  methods: {
    enviarFormulario() {
      console.log(this.form.nombre, this.form.apellido, this.form.email, this.form.password);
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}
div {
  margin-bottom: 1em;
}
label {
  margin-bottom: 0.5em;
}
input {
  padding: 0.5em;
  font-size: 1em;
}
button {
  padding: 0.7em;
  font-size: 1em;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover {
  background-color: #2c8f7c;
}
</style>
