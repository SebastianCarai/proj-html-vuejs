<template>
    <div class="container_65 culinary_collection mt-5 mb-5">
        <!-- Intro titles -->
        <div class="my-5">
            <h3 class="section_title mt-2 mb-4">POPULAR RECIPES</h3>
            <p class="font_m">Aliquam erat volupat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis</p>
        </div>

        <div class="d-flex flex-wrap">
            <div class="card" v-for="(card, index) in cardsArray" :key="index">
                <div>
                    <img :src="require(`../assets/img/${card.imgPath}`)" alt="">
                </div>

                <div class="title">
                    {{card.cardTitle.toUpperCase()}}
                </div>
                </div>
        </div>

    </div>
</template>

<script>

export default {
    name: 'CulinaryCollection',
    components:{
    },
    data: function(){
        return{
            cardsArray:[
                {
                    imgPath: 'drinks-recipes.png',
                    cardTitle: 'Drinks',
                },
                {
                    imgPath: 'soups-recipes.png',
                    cardTitle: 'Soups',
                },
                {
                    imgPath: 'baking-recipes.png',
                    cardTitle: 'Bakery',
                },
                {
                    imgPath: 'dinner-recipes.png',
                    cardTitle: 'Dinner',
                },
                {
                    imgPath: 'healthy-recipes.png',
                    cardTitle: 'Healthy',
                },
                {
                    imgPath: 'staff-picks.png',
                    cardTitle: 'Staff Picks',
                },
                {
                    imgPath: 'premium-recipes.png',
                    cardTitle: 'Appetisers',
                },
                {
                    imgPath: 'quick-easy-recipes.png',
                    cardTitle: 'Quick & Easy',
                },
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.culinary_collection{
    p{
        width: 50%;
        margin: auto;
        text-align: center;
        color: lighten($main_text_color, 20%);
    }
    .card{
        width: calc((100% / 4) - 30px);
        margin: 15px;
        img{
            width: 100px;
        }
        display: inline-block;
        text-align: center;
        .title{
            padding: 10px;
        }
    }
    .card:hover .title{
        background-color: $main-color;
        color: white;
    }
}
</style>