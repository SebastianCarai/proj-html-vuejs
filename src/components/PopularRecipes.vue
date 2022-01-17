<template>
    <div class="container_65 popular_recipes mt-4">
        <div class="my-5">
            <h3 class="section_title mt-2 mb-4">POPULAR RECIPES</h3>
            <p class="font_m">Aliquam erat volupat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis</p>
        </div>

        <div class="d-flex justify-content-between">
            <div class="my_half_col">
                <Card100 v-for="(cardInfo, index) in popularRecipesArray" :key="index" :card100Info="cardInfo"  />
                <div class="orange_btn mx-4"> LEARN MORE </div>
            </div>
            <div class="my_half_col">
                
            </div>
        </div>
    </div>
</template>

<script>
import Card100 from './Card100.vue'

export default {
    name: 'PopularRecipes',
    components:{
        Card100
    },
    data: function(){
        return{
            popularRecipesArray: [
                {
                    imgPath: 'Yogurt-Nan.jpg',
                    cardTitle: 'Lunch Favourite with Salad, Naan And Beans',
                    cardCredits: 'Bakery, Featured, Healthy, Latest Recipes, Staff Picks',
                    cardDescription: 'Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex. Sed porttitor, diam eget convallis volutpat, arcu tellus facilisis nulla, id dignissim orci leo id'
                }
            ]
        }   
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.popular_recipes{
    p{
        width: 50%;
        margin: auto;
        text-align: center;
        color: lighten($main_text_color, 20%);
    }
    .my_half_col{
        width: calc((100% / 2) - 30px);
        background-color: pink;
        height: 100px;
        .orange_btn{
            border-radius: 2px;
        }
    }
}
</style>