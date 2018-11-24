<template>
  <div id="app">
    <h1>practica de inventario de ({ejemplo})</h1>
    <el-radio v-model="radio" label="1">Option A</el-radio>
   <el-radio v-model="radio" label="2">Option B</el-radio>
  </div>
  
</template>

<script>
   export default {
    data () {
      return {
        radio: '1'
      };
    }
  }

</script>

<style>

</style>
