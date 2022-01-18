<template>
    <div class="food_card pb-4">
        <div class="img_container" @mouseover="activateOverlay" @mouseleave="disableOverlay">
            <Overlay :text="foodObject.cardText" :class="{ 'd-none': isOverlayDisabled}"/>
            <img :src="require(`../assets/img/${foodObject.imgPath}`)" :alt="foodObject.cardText">
        </div>
        <h3 class="font_tnr card_title mt-3 mb-2 px-2"> {{ foodObject.cardText }} </h3>
        <div class="card_subtitle px-2">{{foodObject.cardCredits}}</div>
    </div>
</template>

<script>
import Overlay from './Overlay.vue'

export default {
    name: 'FoodCard',
    components:{
        Overlay
    },
    props:{
        foodObject: Object
    },
    data: function(){
        return{
            isOverlayDisabled: true
        }
    },
    methods:{
        activateOverlay: function(){
            this.isOverlayDisabled = false
        },
        disableOverlay: function(){
            this.isOverlayDisabled = true
        }
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
    .img_container{
        position: relative;
        img{
            width: 100%;
        }
    }

}
</style>