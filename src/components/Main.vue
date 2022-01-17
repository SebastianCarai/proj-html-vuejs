<template>
    <main>
        <FoodieJournal />
    </main>
</template>

<script>
import FoodieJournal from './FoodieJournal.vue';

export default {
    name: 'Main',
    components: {
        FoodieJournal
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