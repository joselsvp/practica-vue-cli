<template>
  <h1>Saldo:{{ saldo }}</h1>
  <h1>Cuenta:{{ cuenta }}</h1>
  <h1>Estado: {{ estado ? "Activada" : "Desactivada" }}</h1>
  <h4>Servicios disponibles</h4>
  <div v-for="(item, index) in servicios" :key="index">
     {{index + 1}} - {{item}}
  </div>
  <AccionSaldo texto = "Agregar Saldo" @accion="agregarSaldo"/>
  <AccionSaldo texto = "Disminuir Saldo" @accion="disminuirSaldo" :desactivar="desactivar"/>
</template>

<script>
import AccionSaldo from './AccionSaldo.vue'
export default {
  components: {
    AccionSaldo
  },
  data() {
    return {
      saldo: 1000,
      cuenta: "Visa",
      estado: true,
      servicios: ["pagos", "giros", "transferencias"],
      desactivar: false
    };
  },
  methods: {
    agregarSaldo() {
      this.saldo = this.saldo + 100
      this.desactivar = false
    },
    disminuirSaldo() {
      if(this.saldo <= 0) {
        this.desactivar = true
        alert('saldo agotado')
        return
      }
      this.saldo = this.saldo - 100
    }
  }
};
</script>

<style>
</style>