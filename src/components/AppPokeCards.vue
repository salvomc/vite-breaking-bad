<script>
export default {
    props:{
        myPokeCard: Object
    }
}
</script>

<template>
    <div class="card d-flex my-2 p-3 text-center align-items-center ">
        <img :src="myPokeCard.imageUrl" alt="image">
        <div style="padding-top: 10px">{{ myPokeCard.number }}</div>
        <div><h6>{{ myPokeCard.name }}</h6></div>
        <div>{{ myPokeCard.type1 }}</div>
    </div>

</template>

<style lang="scss" scoped>

    img{
        height: 150px;
        width: 150px;
        background-color: white;
        border-radius: 50%;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 1);
        object-fit: contain;
    }

</style>