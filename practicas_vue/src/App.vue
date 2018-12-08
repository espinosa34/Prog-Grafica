<template>
  <div id="app">
      <h1>Practica de Inventario de Libros</h1>
      <!-- <Visualizar/> -->
      <producto/>
  </div>
</template>

<script>
import visualizar from './components/visualizar.vue'
import inventario from './components/inventario.vue'
import inventario_2 from './components/inventario_2.vue'
import prueba from './components/prueba.vue'

export default {
  name: 'app',
  components: {
    Visualizar,
    inventario
  }
}
</script>

<style>

</style>
