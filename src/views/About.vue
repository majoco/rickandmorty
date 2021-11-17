<template>
  <div class="about">
    <h1>This is {{personajes.name}} detail page</h1>
    <div class="col-3" >
        <div class="caja caja_detalle">
            <img :src="personajes.image">
            <h3>{{personajes.name}}</h3>                        
            <div class="tleft">
              <h4><strong>Specie: </strong>{{personajes.species}}</h4>
              <h4><strong>Status: </strong>{{personajes.status}}</h4>
              <h4><strong>Location: </strong>{{personajes.location.name}}</h4>
            </div>
        </div>
    </div>
    <p>Hecho por <strong>Francisco Javier Ramirez</strong> para su evaluacion</p>
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
        this.consultarPersonaje();
    },
    methods:{
        consultarPersonaje(){
            var idd = this.$route.query.id;          
            fetch('https://rickandmortyapi.com/api/character/'+idd)
            .then(respuesta=>respuesta.json())
            .then((datosRespuesta)=>{
                console.log(datosRespuesta)
                this.personajes = []                
                //if(typeof datosRespuesta[0].success==='undefined'){
                    this.personajes=datosRespuesta;
                //}
            })
            .catch(console.log)
        }
    }
}
</script>