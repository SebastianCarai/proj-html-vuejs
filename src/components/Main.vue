<template>
    <main>
        <FoodieJournal />
        <PopularRecipes />
    </main>
</template>

<script>
import FoodieJournal from './FoodieJournal.vue';
import PopularRecipes from './PopularRecipes.vue';


export default {
    name: 'Main',
    components: {
        FoodieJournal,
        PopularRecipes
    },
    data: function(){
        return{
        }   
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

main{
    background-color: #f5f5f1;
}
</style>