<template>
  <TheHeader v-if="showHeader"/>
  <TheMain/>
  

  <div v-if="acessLevel === 'admin'">Usuario admin</div>
  <div v-else-if="acessLevel === 'marketing'">Usuario Marketing</div>
  <div v-else>Usuario normal</div>


</template>

<script>

import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import axios from 'axios';

axios.get('posts').then(response => {
  console.log(response.data)
})

export default {
  name: 'App',
  components: {
    TheHeader,
    TheMain,
  },
  data() {
    return {
      showHeader: true,
      nome: 'Vinicuis Nunes',
      acessLevel:'marketing'
    }
  },
  filters:{
    currencydecimal(value){
      return value.tofiexed(2)
    }
  },

  mounted(){
    console.log('App.vue montado')
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
/*   -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; */
  height: 100vh;
  display: flex;
  flex-direction: column;
  margin: auto;
  padding: 0%;
 


}
</style>
