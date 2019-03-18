<template>
  
          <div class="conversor">
          <h4>Insira os Números entre virgulas que queira obter a moda</h4>
          <input type="text" v-model="valoresUsuario" placeholder="valores"/>
          <input type="button" value="Calcular" v-on:click="calculoModa"/>
          <h2>{{moda}}</h2>
        
          </div>  

   
</template>


<script>
export default {
    name:"Moda",
  
    data(){
        return{
            moda: [],
            valoresUsuario:"",


        };
    }
,
methods: {
 calculoModa () {
       /* eslint-disable */
       var numbers = this.valoresUsuario.split(",");
     var modes = [], count = [], i, number, maxIndex = 0;
 
    for (i = 0; i < numbers.length; i += 1) {
        number = numbers[i];
        count[number] = (count[number] || 0) + 1;
        if (count[number] > maxIndex) {
            maxIndex = count[number];
        }
    }
 
    for (i in count)
        if (count.hasOwnProperty(i)) {
            if (count[i] === maxIndex) {
                modes.push(Number(i));
            }
        }
         this.moda=modes;
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
