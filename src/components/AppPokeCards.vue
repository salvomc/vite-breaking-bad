<script>
export default {
    props:{
        myPokeCard: Object
    }
}
</script>

<template>
    <div :class="myPokeCard.type1 === 'Grass' ? 'bg-color-grass' : myPokeCard.type1 === 'Fire' ? 'bg-color-fire' : myPokeCard.type1 === 'Water' ? 'bg-color-water' : ''" class="card d-flex my-2 p-3 text-center align-items-center ">
        <img :src="myPokeCard.imageUrl" alt="image">
        <div style="padding-top: 10px">{{ myPokeCard.number }}</div>
        <div><h6>{{ myPokeCard.name }}</h6></div>
        <div>{{ myPokeCard.type1 }}</div>
    </div>

</template>

<style lang="scss" scoped>

    .bg-color-grass{
        background-color: #DEFDE0;
    }

    .bg-color-fire{
        background-color: #FDDFDF;
    }

    .bg-color-water{
        background-color: #DEF3FD;
    }

    img{
        height: 150px;
        width: 150px;
        background-color: white;
        border-radius: 50%;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 1);
        object-fit: contain;
    }

</style>