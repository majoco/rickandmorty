<template>
  <div class="home">    
    <Listar />
    <p>Hecho por <strong>Francisco Javier Ramirez</strong> para su evaluacion</p>
  </div>
</template>

<script>
// @ is an alias to /src
import Listar from '@/components/Listar.vue'

export default {
  name: 'Home',
  components: {
    Listar
  }
}
</script>
