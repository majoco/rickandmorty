<template>
  <div>    
    <div class="container">
      <div class="row">
        <div class="col-md-12">          
          <HelloWorld msg=""/>      
        </div>
      </div>
    </div>
    <Listar />
    <p>Hecho por Francisco Javier Ramirez para su evaluacion</p>
  </div>
</template>

<script>
import Listar from './components/Listar.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {  
  name: 'App',
  components: {
    Listar,
    HelloWorld
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
.caja{
    background: lightgray;
    margin: 5px;
    border-radius: 10px;
    padding-bottom: 10px;
    margin-bottom: 15px;
}
.caja:hover{
  box-shadow: 0px 0px 10px #888888;
}
img{
  width: 100%;
  border-radius: 10px 10px 0px 0px;
}
.row::marker{
  color: transparent;
}

@media screen and (max-width: 992px) {
  .col-3 {      
      max-width: 45%;
      margin: 0px;
      display: inline-block;
  }
  .card-body>.container>.row {
    display: list-item;
  }
}
@media screen and (max-width: 480px) {
  .col-3 {      
    display: contents;
  }
}
</style>
