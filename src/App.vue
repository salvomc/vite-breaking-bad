<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppSelectType from './components/AppSelectType.vue';
import { store } from './store.js';
export default {
  components:{
    AppMain,
    AppHeader,
    AppSelectType
  },
  data(){
    return{
      store
    }
  },
  mounted(){
    this.getPokemonTypes()
  },
  methods:{
    
    getPokemonTypes()
    {
      let myUrl=store.apiUrl;
      if(store.typeValue !== '')
      {
        myUrl += `&eq[type1]=${store.typeValue}`
      }
      axios.get(myUrl).then((response) =>
      {
        store.arrayPokeCards = response.data.docs;
      })
    }
  }
}
</script>

<template>
  
  <div>
    <AppHeader @change="getPokemonTypes"/>
    <AppMain/>
  </div>

</template>

<style lang="scss">
@use './styles/generals.scss' as *;
@use './styles/partials/variables' as *;

</style>