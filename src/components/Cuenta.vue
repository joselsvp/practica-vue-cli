<template>
  <h1>Saldo:{{ saldo }}</h1>
  <h1>Cuenta:{{ cuenta }}</h1>
  <h1>Estado: {{ estado ? "Activada" : "Desactivada" }}</h1>
  <h4>Servicios disponibles</h4>
  <div v-for="(item, index) in servicios" :key="index">
     {{index + 1}} - {{item}}
  </div>
</template>

<script>
export default {
  data() {
    return {
      saldo: 1000,
      cuenta: "Visa",
      estado: true,
      servicios: ["pagos", "giros", "transferencias"],
    };
  },
};
</script>

<style>
</style>