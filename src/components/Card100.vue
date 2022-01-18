<template>
    <div class="card100">
        <div class="img_container" @mouseover="activateOverlay" @mouseleave="disableOverlay">
            <Overlay :text="card100Info.cardTitle" :class="{ 'd-none': isOverlayDisabled}"/>
            <img :src="require(`../assets/img/${card100Info.imgPath}`)" :alt="card100Info.cardTitle">
        </div>
        <div class="p-4">
            <h3 class="font_tnr card_title mt-3 mb-2"> {{card100Info.cardTitle}} </h3>
            <div class="card_subtitle">{{card100Info.cardCredits}}</div>

            <hr>

            <p class="font_m">{{card100Info.cardDescription}}</p>
        </div>
    </div>
</template>

<script>
import Overlay from './Overlay.vue'

export default {
    name: 'Card100',
    components:{
        Overlay
    },
    props:{
        card100Info: Object
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

.card100{
    background-color: white;
    width: 100%;
    .img_container{
        position: relative;
        img{
            width: 100%;
        }
    }
    .card_subtitle{
        color: lighten($main_text_color, 10%);
    }
    p{
        color: lighten($main_text_color, 20%);
    }
}
</style>