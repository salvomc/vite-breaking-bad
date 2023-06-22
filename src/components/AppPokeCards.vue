<script>
export default {
    props:{
        myPokeCard: Object,
    }
}
</script>

<template>
    
    <img :src="myPokeCard.imageUrl" alt="image" class="w-100">
    <h5>{{ myPokeCard.name }}</h5>

</template>

<style lang="scss" scoped>
    
</style>