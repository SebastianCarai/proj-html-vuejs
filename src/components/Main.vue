<template>
    <main>
        <FoodieJournal />
        <PopularRecipes />
        <CulinaryCollection />
        <FarmToTable />
        <Banner />
    </main>
</template>

<script>
import FoodieJournal from './FoodieJournal.vue';
import PopularRecipes from './PopularRecipes.vue';
import CulinaryCollection from './CulinaryCollection.vue';
import FarmToTable from './FarmToTable.vue';
import Banner from './Banner.vue';




export default {
    name: 'Main',
    components: {
        FoodieJournal,
        PopularRecipes,
        CulinaryCollection,
        FarmToTable,
        Banner
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