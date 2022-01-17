<template>
    <div class="container_65 foodie_journal">
        <h3 class="section_title mt-2 mb-4">FOODIE JOURNAL</h3>
        <div class="d-flex justify-content-between">
            <div class="card_container" v-for="(singleInfo, index) in foodieJournalArray" :key="index">
                <FoodCard :foodieArray="singleInfo" />
            </div>
        </div>
    </div>
</template>

<script>
import FoodCard from './FoodCard.vue'

export default {
    name: 'FoodieJournal',
    components:{
        FoodCard
    },
    data: function(){
        return{
            foodieJournalArray:[
                {
                    imgPath: 'single-post-img3-400x263.jpg',
                    cardText: 'Food Corner: Top Japanese Restaurants for Sushi',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                {
                    imgPath: 'fi-roundup-400x263.jpg',
                    cardText: 'Roundup: My New Favourite Recipes For Halty Living',
                    cardCredits: 'By admin | March 25th, 2019'
                },
                {
                    imgPath: 'fi-toasts-400x263.jpg',
                    cardText: 'Why These Toasts with Tea are My New Favorite',
                    cardCredits: 'By admin | March 25th, 2019'
                }
            ]
        }   
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.foodie_journal{
    background-color: white;
    padding: 30px;
    position: relative;
    top: -50px;
    .section_title{
        &::before{
            display: inline-block;
            content: '';
            width: 400px;
            height: 2px;
            margin: 0 30px;
            vertical-align: middle;
            background-color: #e0dede;
        }
        &::after{
            display: inline-block;
            content: '';
            width: 400px;
            height: 2px;
            margin: 0 30px;
            vertical-align: middle;
            background-color: #e0dede;
        }
    }
    .card_container{
        width: calc((100% / 3) - 20px);
    }

}
</style>