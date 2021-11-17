<template>
  <div class="container">    

    <div class="card">
        <div class="card-header">
            Personajes de Rick and Morty
        </div>
        <div class="card-body">

            <div class="container">
                <div class="row">                    
                    <div class="col-3" v-for="personaje in personajes" :key="personaje.id">
                        <div class="caja">
                            <img :src="personaje.image">
                            <h3>{{personaje.name}}</h3>                        
                            <a class="btn btn-info" :href="'/personaje/' + personaje.id">Detalle</a>
                        </div>
                    </div>                    
                </div>
            </div>
                
        </div>
    </div>    
  </div>
</template>

<script>
export default {
    data(){
        return{
            personajes:[]
        }        
    },

    created:function(){
        this.consultarPersonajes();
    },
    methods:{
        consultarPersonajes(){
            fetch('https://rickandmortyapi.com/api/character/')
            .then(respuesta=>respuesta.json())
            .then((datosRespuesta)=>{
                console.log(datosRespuesta)
                this.personajes = []
                //if(typeof datosRespuesta[0].success==='undefined'){
                    this.personajes=datosRespuesta.results;
                //}
            })
            .catch(console.log)
        }
    }
}
</script>

<style scoped lang="scss">
</style>
