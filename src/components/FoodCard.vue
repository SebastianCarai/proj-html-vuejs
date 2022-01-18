<template>
    <div class="food_card pb-4">
        <img :src="require(`../assets/img/${foodObject.imgPath}`)" alt="">
        <h3 class="font_tnr card_title mt-3 mb-2"> {{ foodObject.cardText }} </h3>
        <div class="card_subtitle">{{foodObject.cardCredits}}</div>
    </div>
</template>

<script>
export default {
    name: 'FoodCard',
    props:{
        foodObject: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.food_card{
    background-color: white;
    width: 100%;
    text-align: center;
    img{
        width: 100%;
    }
}
</style>