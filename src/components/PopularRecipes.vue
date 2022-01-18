<template>
    <div class="container_65 popular_recipes mt-4">
        <!-- Intro titles -->
        <div class="my-5">
            <h3 class="section_title mt-2 mb-4">POPULAR RECIPES</h3>
            <p class="font_m">Aliquam erat volupat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis</p>
        </div>

        <!-- Main content -->
        <div class="d-flex justify-content-between">
            <div class="my_half_col">
                <Card100 v-for="(cardInfo, index) in popularRecipesArray" :key="index" :card100Info="cardInfo"  />
                <div class="orange_btn mx-4"> LEARN MORE </div>
            </div>
            <div class="my_half_col d-flex row-cols-2 flex-wrap">
                <div class="px-3 pb-4" v-for="(imagePath,index) in imgsArray" :key="index"><img :src="require(`../assets/img/${imagePath}`)" alt=""></div>
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
            ],
            imgsArray:[
                'Mixed-fruits-1200x790.jpg',
                'r-rachel-park-366508-unsplash-min-1200x790.jpg',
                'r-michelle-tsang-500721-unsplash-min-1200x790.jpg',
                'quick-summer-drink-460x295.jpg',
                'r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg',
                'perfect-cosmopolitan-460x295.jpg',
                'fi2x-6-460x295.jpg',
                'r-brooke-lark-96398-unsplash-min-460x295.jpg',
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
        width: calc((100% / 2) - 20px);
        .orange_btn{
            border-radius: 2px;
        }
        img{
            width: 100%;
        }
    }
}
</style>