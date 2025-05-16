<template>
  <div class="container">
    <label for="id_nombre"> Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />

    <label for="id_apellido"> Apellido:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />

    <label for="id_edad">Edad:</label>
    <input v-model="nuevaEdad" id="id_edad" type="number" />

    <label for="id_carrera">Carrera:</label>
    <input v-model="nuevaCarrera" id="id_carrera" type="text" />

    <label for="id_correo">Correo:</label>
    <input v-model="nuevoCorreo" id="id_correo" type="email" />

    <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>


    <ul>
      <li v-for="{nombre, apellido, edad, carrera, correo} in lista" :key="nombre">
       <strong>Nombre:</strong>{{ nombre }}- <strong>Apellido:</strong>{{ apellido }}- <strong> Edad:</strong>{{ edad }}-
        <strong>Carrera:</strong> {{ carrera }} <strong>-Correo:</strong>{{ correo }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "",
      nuevoApellido: "",
      nuevaEdad: "",
      nuevaCarrera: "",
      nuevoCorreo: "",
      lista: [
  {
    nombre: "Angelo",
    apellido: "Pujota",
    edad: 22,
    carrera: "Ingeniería",
    correo: "angelo@example.com",
  },
  {
    nombre: "Pedro",
    apellido: "Guaycha",
    edad: 23,
    carrera: "Administración",
    correo: "pedro.guaycha@example.com",
  },
  {
    nombre: "Juan",
    apellido: "Teran",
    edad: 21,
    carrera: "Psicología",
    correo: "juan.teran@example.com",
  },
  {
    nombre: "Marco",
    apellido: "Andrade",
    edad: 24,
    carrera: "Medicina",
    correo: "marco.andrade@example.com",
  },
  {
    nombre: "Andrea",
    apellido: "Castillo",
    edad: 20,
    carrera: "Derecho",
    correo: "andrea.castillo@example.com",
  },
  {
    nombre: "Marcelo",
    apellido: "Lopez",
    edad: 25,
    carrera: "Arquitectura",
    correo: "marcelo.lopez@example.com",
  },
  {
    nombre: "Alejandra",
    apellido: "Pineda",
    edad: 22,
    carrera: "Diseño Gráfico",
    correo: "alejandra.pineda@example.com",
  },
],
    };
  },
  methods: {
     agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
        edad: this.nuevaEdad,
        carrera: this.nuevaCarrera,
        correo: this.nuevoCorreo,
      };
      this.lista.unshift(nuevo);
    },
  },
};
</script>

<style>
.container{
  display: flex;
  flex-direction: column;
  gap: 5px;
  max-width: 400px;
  margin: 0 auto;
}
button {
  padding: 8px;
  background-color: #3498db;
  color: white;
  border: solid;
}
ul {
  margin-top: 20px;
  text-align: left;
}
</style>