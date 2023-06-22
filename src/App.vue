<script>
import axios from 'axios';
import AppMain from './components/AppMain.vue';
import { store } from './store.js';
export default {
  components:{
    AppMain
  },
  data(){
    return{
      store
    }
  },
  mounted(){
    axios.get(store.apiUrl).then((response) => 
    {
      store.arrayPokeCards = response.data.docs;
    })
  }
}
</script>

<template>
  
  <div>
    <AppMain/>
  </div>

</template>

<style lang="scss">
@use './styles/generals.scss' as *;
@use './styles/partials/variables' as *;

</style>