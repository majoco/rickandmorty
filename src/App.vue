<template>
  <div>    
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div>
            <router-view></router-view>
          </div>
          <div>
            <router-view></router-view>
          </div>
        </div>
      </div>
    </div>
    <Listar />
  </div>
</template>

<script>
import Listar from './components/Listar.vue'

export default {
  name: 'App',
  components: {
    Listar
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
img{
  width: 100%;
  border-radius: 10px 10px 0px 0px;
}
</style>
