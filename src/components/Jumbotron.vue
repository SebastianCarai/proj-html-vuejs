<template>
    <div class="jumbotron central_align">
        <div class="jumbo_content">
            <div class="orange_btn"> TODAY'S PICK </div>
            <h1 class="jumbo_text font_tnr"> Food Corner: Top Japanese Restaurants for Sushi </h1>
            <h3 class="mt-3 font_tnr">March 25, 2019</h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Jumbotron',
    data: function(){
        return{
        }   
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';
.jumbotron{
    height: 700px;
    background-image: url('../assets/img/single-post-img3.jpg');
    background-position: center;
    object-fit: cover;
    & > .jumbo_content{
        position: relative;
        background-color: white;
        padding: 50px 70px;
        border-radius: 15px;
        text-align: center;
        color: $main_text_color;
        width: 40%;
        margin: auto;
        .orange_btn{
            font-weight: 600;
            border-radius: 10px;
            position: absolute;
            top: 0;
            transform: translate(-50%, -50%);
            font-size: 16px;
        }
        h1{
            font-size: 50px;
            font-weight: 600;
        }
        h3{
            font-size: 20px;
            color: lighten($main_text_color, 20%);
            font-weight: 600;
        }
    }
}
</style>