<script>
import AppPokeCards from './AppPokeCards.vue';
import { store } from '../store.js'
export default {
    components:{
        AppPokeCards
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    
    <main>
       <div class="container p-5 mt-3 mb-3 bg-white rounded">
            <div class="row d-flex overflow-auto bg-secondary custom-row">
                <div v-for="(card, index) in store.arrayPokeCards" :key="index" class="col-lg-2 col-md-4 col-6" style="width: 20%;">
                    <AppPokeCards :myPokeCard="card" />
                </div>
            </div>
       </div> 
    </main>

</template>

<style lang="scss" scoped>
    .custom-row{
        height: 572px;
        border-radius: 10px;
    }

</style>