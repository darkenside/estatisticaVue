<template>
  
          <div class="conversor">
          <h4>Insira os Números entre virgulas que queira obter o desvio padrão</h4>
          <input type="text" v-model="valoresUsuario" placeholder="valores"/>
          <input type="button" value="Calcular" v-on:click="calculoDesvioPadrao"/>
          <h2>{{desvioPadrao}}</h2>
        
          </div>  

   
</template>


<script>
export default {
    name:"Conversor",
  
    data(){
        return{
            desvioPadrao: 0,
            valoresUsuario:"",


        };
    }
,
methods: {
 calculoDesvioPadrao () {
       
       var valores = this.valoresUsuario.split(",");
       var total =0;
       var numeros=0;
      
       for (var i=0; i<valores.length ;i++){
          
           total = total + parseFloat(valores[i]);
           ++numeros;
          
       }
    
       var media = parseFloat(parseFloat(total)/numeros) ; 
        
       var calc = parseFloat(0.00);
        for (var i=0; i<valores.length ;i++){
         
         calc =calc + ((valores[i] - media) * (valores[i] - media));
       // window.alert(calc);

       }
    
        this.desvioPadrao=Math.sqrt((calc/numeros));

     
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
