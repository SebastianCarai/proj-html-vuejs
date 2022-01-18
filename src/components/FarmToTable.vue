<template>
    <div class="container_65 farm_to_table mb-5">
        <!-- Intro titles -->
        <div>
            <div class="intro_titles">
                <h3 class="section_title mt-2 mb-4">FARM TO TABLE</h3>
                <p class="font_m">Aliquam erat volupat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis</p>
            </div>

            <div class="orange_btn">
                READ OUR BLOG <i class="fas fa-book-reader"></i>
            </div>
        </div>

        <!-- MAIN CONTENT -->
        <div class="d-flex justify-content-between">

            <!-- Left column -->
            <div class="left_col">
                <Card100 :card100Info="cardInfo"/>
                <div class="d-flex justify-content-between px-4 pb-4 comments_messages">
                    <span class="load_more"> Read More <i class="fas fa-chevron-right"></i> </span>
                    <span class="comments_number"> <i class="far fa-comments"></i> 0</span>
                </div>

                <div class="mt-5 d-flex justify-content-between flex-wrap">
                    <FoodCard v-for="(singleCard,index) in foodCardsArray" :key="index" :foodObject="singleCard" class="single_card mb-4"/>
                </div>

                <div class="load_more_posts">
                    LOAD MORE POSTS
                </div>
            </div>

            <!-- Right column -->
            <div class="right_col">
                ciao
            </div>
        </div>

    </div>
</template>

<script>
import Card100 from './Card100.vue'
import FoodCard from './FoodCard.vue'


export default {
    name: 'FarmToTable',
    components:{
        Card100,
        FoodCard
    },
    data: function(){
        return{
            // Info for the big card100
            cardInfo: {
                imgPath: 'single-post-img3.jpg',
                cardTitle: 'Food Corner: Top Japanese resturants for Sushi',
                cardCredits: 'BY admin | March 25th, 2019',
                cardDescription: 'Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex. Sed porttitor, diam eget convallis volutpat, arcu tellus facilisis nulla, id dignissim orci leo id'
            },
            // Info for the little FoodCards
            foodCardsArray: [
                {
                    imgPath: 'fi-roundup.jpg',
                    cardText: 'Roundup: My New Favourtite Riceps For Healthy Living',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                                {
                    imgPath: 'fi-korean-food.jpg',
                    cardText: 'Meal Prep: Korean Bibimbap with Kimchi',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                                {
                    imgPath: 'fi-toasts.jpg',
                    cardText: 'Why These Toasts with Tea are My New Favorite',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                                {
                    imgPath: 'fi-street-food.jpg',
                    cardText: 'Exploring Street Food in Bangkok',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                                {
                    imgPath: 'fi-organic-breakfast.jpg',
                    cardText: 'Organic Choices For Healthier Living',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                                {
                    imgPath: 'fi-water-side-rest.jpg',
                    cardText: '5 Waterside Restaurants in Istanbul for Special Events',
                    cardCredits: 'By admin | March 25th, 2019'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.container_65.farm_to_table{
    margin-top: 150px;

    // INTRO
    .intro_titles{
        width: 50%;
        display: inline-block;
        p{
            color: lighten($main_text_color, 20%);
        }
        & .section_title{
            text-align: left;
        }
    }
    .orange_btn{
        float: right;
        border-radius: 3px;
    }

    // MAIN CONTENT
    .left_col{
        width: 58%;
        .comments_messages{
            background-color: white;
        }
        .load_more{
            color: lighten($main_text_color, 10%);
            cursor: pointer;
        }
        .comments_number{
            font-weight: 600;
        }
        .single_card{
            width: calc(50% - 20px);
        }
        .load_more_posts{
            padding: 20px;
            text-align: center;
            background-color: #edede7;
            color: $main_text_color;
            font-weight: 600;
            cursor: pointer;
        }
    }
    .right_col{
        width: 34%;
        background-color: pink;
    }
}
</style>