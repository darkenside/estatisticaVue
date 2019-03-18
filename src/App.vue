<template>
  <div id="app">
    <div class="linha">
    <h1 class="text-center">Desvio Padrão</h1>
    <h1 class="text-center">Mediana</h1>
    </div>
      <div class="linha">
    <DesvioPadrao moedaA="USD" moedaB="BRL"/>
    <Mediana moedaA="USD" moedaB="BRL"/>
  </div>
   <div class="linha">
   <h1 class="text-center">Media</h1>
    <h1 class="text-center">Moda</h1>
    </div>
      <div class="linha">
    <Media moedaA="USD" moedaB="BRL"/>
    <Moda moedaA="USD" moedaB="BRL"/>
  </div>
 <br><br><br><br><br><br><br>
  <h2>Desenvolvido Por Omalotech - 2019</h2>
  </div>
</template>

<script>

import DesvioPadrao from "./components/DesvioPadrao.vue";
import Mediana from "./components/Mediana.vue";
import Media from "./components/Media.vue";
import Moda from "./components/Moda.vue";
export default {
  name: "app",
  components: {
    DesvioPadrao,
    Mediana,
    Media,
    Moda
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.linha{
  margin-top: 40px;
display: flex;
justify-content: space-around;

}
.text-center {

  text-align: center;
  color: darkgray
}

.rodape{
position: absolute;
bottom: 0;

}

</style>
