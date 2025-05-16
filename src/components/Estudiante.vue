<template>
  <div class="container">
    <label for="id_nombre"> Nombre:</label>
     <label for="id_apellido"> Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
     <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <button v-on:click ="agregarEstudiante()">Agregar Estudiante</button>
    {{ nuevoNombre }}
    <ul>
      <li v-for="{ nombre, apellido } in lista" :key="nombre">
        Nombre: {{ nombre }} -Apellido:{{ apellido }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "Nombre",
      nuevoApellido:"Apellido",
      lista: [
        { nombre: "Angelo", apellido: "Pujota" },
        { nombre: "Pedro", apellido: "Guaycha" },
        { nombre: "Juan", apellido: "Teran" },
        { nombre: "Marco", apellido: "Andrade" },
        { nombre: "Andrea", apellido: "Castillo" },
        { nombre: "Marcelo", apellido: "Lopez" },
        { nombre: "Alejandra", apellido: "Pineda" },
      ],
    };
  },
  methods:{
    agregarEstudiante(){
        const nuevo= {
            nombre:this.nuevoNombre,
            apellido:this.nuevoApellido,
        }
        this.lista.unshift(nuevo);
    }
  }
};
</script>

<style>
</style>