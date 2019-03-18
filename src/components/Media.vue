<template>
  
          <div class="conversor">
          <h4>Insira os Números entre virgulas que queira obter a media</h4>
          <input type="text" v-model="valoresUsuario" placeholder="valores"/>
          <input type="button" value="Calcular" v-on:click="calculoMedia"/>
          <h2>{{media}}</h2>
        
          </div>  

   
</template>


<script>
export default {
    name:"Media",
  
    data(){
        return{
            media: 0,
            valoresUsuario:"",


        };
    }
,
methods: {
 calculoMedia () {
       /* eslint-disable */
       var valores = this.valoresUsuario.split(",");
       var total =0;
       var numeros=0;
      
       for (var i=0; i<valores.length ;i++){
          
           total = total + parseFloat(valores[i]);
           ++numeros;
          
       }
    
       this.media = parseFloat(parseFloat(total)/numeros) ; 
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
