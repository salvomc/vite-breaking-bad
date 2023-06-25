<script>
import { store } from '../store';

export default {
    components:{
    },
    data(){
        return{
            store,
            pokemonType:
                    [
                        "Bug",
                        "Dark",
                        "Dragon",
                        "Electric",
                        "Fairy",
                        "Fighting",
                        "Fire",
                        "Flying",
                        "Ghost",
                        "Grass",
                        "Ground",
                        "Ice",
                        "Normal",
                        "Poison",
                        "Psychic",
                        "Rock",
                        "Steel",
                        "Water",
                    ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row d-flex mt-3 mb-2">
                <div class="circle blue"></div>
                <div class="circle red"></div>
                <div class="circle yellow"></div>
                <div class="circle green"></div>
                <div class="select-type-container">
                <select class="select-type" v-model="store.typeValue" @change="$emit('typeChange')">
                    <option value="" selected>Select type</option>
                    <option v-for="(type, index) in pokemonType" :key="index" :value="type" >{{ type }}</option>
                </select>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    
    .circle{
        border: 4px solid white;
        margin-left: 15px;
    }
    .blue{
        height: 130px;
        width: 130px;
        border-radius: 50%;
        background: rgb(0,45,240);
        background: linear-gradient(325deg, rgba(0,45,240,1) 20%, rgba(255,255,255,1) 90%);
    }
    .red{
        height: 40px;
        width: 40px;
        border-radius: 50%;
        background: rgb(240,0,0);
        background: linear-gradient(325deg, rgba(240,0,0,1) 20%, rgba(255,255,255,1) 90%);
    }
    .yellow{
        height: 40px;
        width: 40px;
        border-radius: 50%;
        background: rgb(226,240,0);
        background: linear-gradient(325deg, rgba(226,240,0,1) 20%, rgba(255,255,255,1) 90%);
    }
    .green{
        height: 40px;
        width: 40px;
        border-radius: 50%;
        background: rgb(12,175,11);
        background: linear-gradient(325deg, rgba(12,175,11,1) 20%, rgba(255,255,255,1) 90%);
    }
    .select-type-container{
        margin-left: 13px;
        display: flex;
        justify-content: end;
    }
    .select-type{
        width: 20%;
    }

</style>