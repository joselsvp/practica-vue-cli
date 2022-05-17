<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <TituloBanco texto = "Este es el titulo de mi banco"/>
</template>

<script>
import TituloBanco from './components/TituloBanco.vue'

export default {
  name: 'App',
  components: {
    TituloBanco
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
