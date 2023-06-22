<script>
import AppPokeCards from './AppPokeCards.vue';
import { store } from '../store.js'
export default {
    components:{
        AppPokeCards,
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    
    <div>
       <div class="container">
        <div class="row d-flex justify-between">
            <div v-for="(card, index) in store.arrayPokeCards" :key="index" class="col-2 mx-2">
                <AppPokeCards :myPokeCard="card" />
            </div>
        </div>
       </div> 
    </div>

</template>

<style lang="scss" scoped>
    
</style>