<template>
  
          <div class="conversor">
          <h4>Insira os Números entre virgulas que queira obter a mediana</h4>
          <input type="text" v-model="valoresUsuario" placeholder="valores"/>
          <input type="button" value="Calcular" v-on:click="calculoMediana"/>
          <h2>{{mediana}}</h2>
        
          </div>  

   
</template>


<script>
export default {
    name:"Mediana",
  
    data(){
        return{
            mediana: 0,
            valoresUsuario:"",


        };
    }
,
methods: {
 calculoMediana () {
       /* eslint-disable */
       var values = this.valoresUsuario.split(",");
       
        values.sort( function(a,b) {return a - b;} );

      var half = Math.floor(values.length/2);

      if(values.length % 2){
        this.mediana= values[half];
        }
     else{
         this.mediana= (((parseFloat(values[half-1]) + parseFloat(values[half]))) / 2);
    
     }
    } 

  }
};
</script>


<style scoped>
.conversor {
  max-width: 300px;
  padding: 20px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2)


}


</style>
