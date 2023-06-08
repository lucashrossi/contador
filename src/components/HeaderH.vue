<template>
    <div class="centro">


      <h2>{{tituloh}}</h2>
      
      <p>{{numero}}</p>

      <h2>{{total}}</h2>
      <h4>{{fecha}}</h4>
    </div>
</template>

<script>
export default {
  name: 'HeaderH',
  props: { 
    numero: Number,
    tituloh: String,
    total: Number,
    fecha: Date
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.centro {
    text-align: center;
}
</style>
