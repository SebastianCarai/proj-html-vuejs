<template>
    <div class="container_65 farm_to_table">
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

                <!-- Last recipes -->
                <div class="last_recipes">
                    <img src="../assets/img/ad-bg.jpg" alt="">
                    <div>VIEW OUR LATEST RECIPES</div>
                </div>

                <!-- City Guide -->
                <div class="city_guide mt-5">
                    <div class="city_guide_photo">
                        <img src="../assets/img/singapore-featured-image.jpg" alt="">
                        <div>City Guide: Singapore</div>
                    </div>
                    <a href="#" class="view_city_guides"> <i class="fas fa-globe-americas"></i> VIEW ALL CITY GUIDES </a>
                </div>

                <hr class="my-5">

                <!-- Search -->
                <div class="search">
                    <input type="text" placeholder="Search...">
                    <i class="fas fa-search"></i>
                </div>

                <!-- Socials -->
                <div class="follow_us">
                    <h4 class="font_tnr mt-5 mb-3"> Follow Us</h4>
                    
                    <ul>
                        <li class="d-inline-block">
                            <a href="https://www.facebook.com"><i class="fab fa-facebook-f"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="https://www.instagram.com"><i class="fab fa-instagram"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="https://www.twitter.com"><i class="fab fa-twitter"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="https://www.youtube.com"><i class="fab fa-youtube"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="https://www.youtube.com"><i class="fab fa-pinterest-p"></i></a>
                        </li>
                    </ul>
                </div>

                <!-- Tweets -->
                <div class="tweets mt-5">
                    <div class="d-flex">
                        <div class="font_tnr type_of_comments d-flex align-items-center justify-content-center active">Popular</div>
                        <div class="font_tnr type_of_comments d-flex align-items-center justify-content-center">Recent</div>
                    </div>

                    <div class="single_tweet d-flex align-items-center mt-4" v-for="(tweet,index) in tweetsArray" :key="index">
                        <div class="tweet_img">
                            <img :src="require(`../assets/img/${tweet.path}`)" alt="">
                        </div>
                        <div class="tweet_content">
                            <div class="tweet_text">{{tweet.text}}</div>
                            <div class="tweet_date">{{tweet.date}}</div>
                        </div>
                    </div>

                    <TweetCard />
                </div>

            </div>
        </div>

    </div>
</template>

<script>
import Card100 from './Card100.vue'
import FoodCard from './FoodCard.vue'
import TweetCard from './TweetCard.vue'


export default {
    name: 'FarmToTable',
    components:{
        Card100,
        FoodCard,
        TweetCard
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
            ],
            tweetsArray:[
                {
                    path: 'single-post-img3-150x150.jpg',
                    text: 'Food Corner: Top Japanese Restaurants for Sushi',
                    date: 'March 25th, 2019'
                },
                {
                    path: 'singapore-featured-image-150x150.jpg',
                    text: 'City Guide: Singapore',
                    date: 'February 27th, 2019'
                },
                {
                    path: 'slide1-bg-150x150.jpg',
                    text: '6 Nutritional Tips to Help Burn body Fat',
                    date: 'February 28th, 2019'
                }
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
    padding-bottom: 100px;

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
        width: 61%;
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
        width: 33%;
        img{
            width: 100%;
        }

        // Last recipes
        .last_recipes{
            height: 450px;
            overflow: hidden;
            position: relative;
            & > img{
                position: absolute;
                left: 50%;
                top: 50%;
                transform: translate(-50%, -50%);
            }
            & > div{
                font-size: 25px;
                text-align: center;
                width: 30%;
                position: absolute;
                left: 50%;
                top: 50%;
                transform: translate(-50%, -50%);
                z-index: 1;
            }
        }
        // City guide
        .city_guide_photo{
            position: relative;
            & > div{
                position: absolute;
                bottom: 40px;
                background-color: rgba(#000000, $alpha: 0.6);
                z-index: 1;
                font-size: 19px;
                font-weight: 600;
                color: white;
                padding: 15px;
            }
        }
        .view_city_guides{
            display: block;
            text-align: center;
            padding: 10px;
            background-color: $main_color;
            color: white;
            font-size: 15px;
            font-weight: 600;
        }
        // Search
        .search{
            position: relative;
            input{
                padding: 13px 50px;
                width: 100%;
                border-radius: 5px;
                border: 1px solid #aaaaaa;
            }
            i{
                position: absolute;
                top: 50%;
                left: 20px;
                transform: translateY(-50%);
                color: #aaaaaa;
            }
        }
        // Socials
        .follow_us{
            h4{
                font-size: 20px;
                font-weight: 600;
                color: $main_color;
            }
            li{
                height: 40px;
                width: 40px;
                border-radius: 10px;
                background-color:#edede8;
                margin-right: 10px;
                position: relative;
                font-size: 20px;
                color: #67615a;
                a{
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                }
            }
        }
        // Twitts
        .tweets{
            .type_of_comments{
                cursor: pointer;
                width: 50%;
                font-size: 18px;
                background-color: #f5f5f1;
                border: 1px solid #e9e8e7;
                padding: 13px;
                &.active{
                    background-color: white;
                }
            }
        }
        .single_tweet{
            .tweet_img{
                width: 20%;
                padding: 10px;
                img{
                    border-radius: 50%;
                }
            }
            .tweet_content{
                width: 80%;
                .tweet_text{
                    color: $main_text_color;
                    font-size: 17px;
                }
                .tweet_date{
                    font-size: 13px;
                    color: lighten($main_text_color, 20%);
                }
            }
        }

    
    }
}
</style>