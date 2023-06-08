<template>
  <div id="app">
   

    <h1>{{titulo}}</h1>

      <button v-on:click="suma" value="Click">Suma</button>
      <button v-on:click="resta" value="Click">Resta</button>

   

      <HeaderH :numero="numero" :tituloh="tituloh" :total="total" :fecha="fecha" />

  </div>
</template>

<script>

import HeaderH from './components/HeaderH.vue'

export default {
  name: 'App',
  components: {
    HeaderH
  },
  data() {
        return {
            titulo: "Contador",
            numero: 5,
            tituloh: "",
            foto: "./2023.png",
            total: 0,
            fecha: 0
           
        }
    },
    created() {
        this.calculo()
    },
    methods: {
        calculo() {
            this.total = 
            this.numero = 10
            this.tituloh =  "-"
            this.fecha = Date(this.fecha).toString()
        
        },
        suma() {
            this.total += this.numero 
            this.numero += 1
            this.tituloh =  "Sumaste!"
            this.fecha = Date(this.fecha).toString()
                
        },
        resta() {
            this.total -= this.numero
            this.numero -= 1
            this.tituloh =  "Restaste!"
            this.fecha = Date(this.fecha).toString()
             
        }
    },
    computed: {
        
    }
}
</script>

<style>
#app {
  
  text-align: center;
  margin-top: 60px;
}
</style>
