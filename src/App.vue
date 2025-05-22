<template>
  <!--<hm/> -->
  <!--<Contador/>-->
  <!--<EstudianteView/>-->
 <!-- <EstudianteTablaView/>-->
 <!-- <FormularioView/>-->
 <PreguntaView/>
</template>

<script>
import hm from './views/HolaMundoView.vue'
import Contador from "@/views/ContadorView.vue"
import EstudianteView from "@/views/EstudianteView.vue"
import EstudianteTablaView from './views/EstudianteTablaView.vue'
import FormularioView from './views/FormularioView.vue'
import PreguntaView from './views/PreguntaView.vue'

export default {
  name: 'App',
  components: {
    hm,
    Contador,
    EstudianteView,
    EstudianteTablaView,
    FormularioView,
    PreguntaView,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
