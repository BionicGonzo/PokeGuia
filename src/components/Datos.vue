<template>
  <div>
    <h2>{{ msg }}</h2>
    <img v-bind:src="laImagen" alt="">
    <h2>Movimientos</h2>
    <ul>
      <li v-for="movimiento in listaMovimientos" :key="movimiento">
        {{ movimiento.move.name }}
      </li>
    </ul>
    <h2>Habilidades</h2>
    <ul>
      <li v-for="habilidad in listaHabilidades" :key="habilidad">
        {{ habilidad.ability.name }}
      </li>
    </ul>
    <footer>
      <h6>Gonzalo Araos • Bootcamp Front End 0012, 2022</h6>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Datos',
  props: {
    msg: String,
    laImagen:'',
    listaMovimientos: [],
    listaHabilidades:[],
  },
  data(){
    return{
    otraLista:[],
    }//Fin return
  }//Fin data
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h2 {
  background-color: rgba(0, 0, 0, 0.7);
  margin: 50px;
  border: 1px solid #FFCC00;
}
ul {
  background-color: rgba(0, 0, 0, 0.7);
  list-style-type: none;
  padding: 0 20px;
  margin: 50px;
  border: 1px solid #FFCC00;
}
li {
  display: inline-block;
  margin: 5px 10px;
}

a {
  color: #42b983;
}

footer {
  padding: 10px;
}
</style>
