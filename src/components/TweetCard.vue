<template>
    <div class="tweet_card mt-4">
        <!-- Tweet top part -->
        <div class="d-flex justify-content-between">
            <div class="left_top_part">
                <span>Tweets </span>
                 by <a href="#" class="post_author">@Theme_Fusion</a>
            </div>
            <div>
                <img src="../assets/img/image.svg" alt="">
            </div>
        </div>

        <!-- Tweet content-->
        <div class="d-flex mt-3 tweet_top">
            <div>
                <div class="user_logo">
                    <img src="../assets/img/3a74ce3d0532b7773b174c45ca3bd05a_bigger.png" alt="">
                </div>
            </div>
            <div class="tweet_content mx-2">
                <h5>ThemeFusion</h5>
                <div>@Theme_Fusion</div>
                <p>Do you need sublime WordPress hosting for your next website?
                    Take advantage of exclusive parnter offers that we have secured just for you,
                    & launch your site in seconds with <a href="#">#avada</a> on WP Engine hosting & get 30% Off this Black Friday <br>
                    <a href="#">bit.ly/3kjLLe2</a> <a href="#">#BlackFriday2020</a>
                </p>
                <img src="../assets/img/En2TRxLW4AEiWUN.jpeg" alt="" class="wp_photo">
                <div class="d-flex justify-content-between mt-2 bottom_actions">
                    <div>
                        <i class="far fa-heart"></i>
                        <i class="fas fa-share-square mx-3"></i>
                    </div>
                    <div>
                        21h
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TweetCard'
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.tweet_card{
    background-color: white;
    padding: 20px;
    .left_top_part{
        font-size: 12px;
        &>span{
            font-size: 22px;
        }
        .post_author{
            color: #2b7bb9;
        }
    }
    .tweet_top{
        .user_logo{
            border-radius: 50%;
            overflow: hidden;
            img{
                width: 35px;
            }
        }
        .tweet_content{
            h5{
                font-weight: 800;
                font-size: 15px;
                margin-bottom: 0;
            }
            div{
                font-size: 13px;
                color: lighten($main_text_color, 30%);
            }
            p{
                font-size: 14px;
                a{
                    color: #2b7bb9;
                }
            }
            .wp_photo{
                width: 100%;
                border-radius: 8px;
            }
            .bottom_actions {
                i{
                font-size: 17px;
                }
            }
        }
    }

}
</style>