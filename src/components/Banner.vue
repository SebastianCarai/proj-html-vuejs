<template>
    <div>

        <!-- Subscribe for free book -->
        <div class="banner d-flex justify-content-center align-items-center">
            <div>
                <div class="banner_title font_tnr mb-3">
                    Subscribe <span> & </span> Receive a Free Book
                </div>
                <p class="font_m">Aliquam erat volupat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis</p>
                <div class="my-5">
                    <input type="email" placeholder="Insert your email...*">
                    <span class="orange_btn">SUBSCRIBE </span>
                </div>
                <div class="baner_credits">Cras porttitor pellentesque sem eu pretium</div>
            </div>
        </div>

        <!-- Photos -->
        <div class="d-flex flex-wrap">
            <div class="img_container" v-for="(singleImage,index) in images" :key="index">
                <img :src="require(`../assets/img/${singleImage}`)" alt="">
            </div>
        </div>
    </div>

</template>

<script>
// import Overlay from './Overlay.vue'

export default {
    name: 'Banner',
    data: function(){
        return{
            images:['Yogurt-Nan.jpg','Mixed-fruits.jpg','r-rachel-park-366508-unsplash-min.jpg','r-michelle-tsang-500721-unsplash-min.jpg']
        }
    },
    components:{
        // Overlay
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

// Subscribe for free book banner
.banner{
    height: 450px;
    background-image: url('../assets/img/subscribe-sec-bg.png');
    background-size: cover;
    background-position: center;
    text-align: center;
    & > div{
        .banner_title{
            font-size: 35px;
            font-weight: 600;
            color: $main_text_color;
            span{
                color: $main_color;
            }
        }
        width: 40%;
        p{
            color: lighten($main_text_color, 20%);
        }
        input{
            padding: 13px 20px;
            margin-right: 20px;
            width: 60%;
            border-radius: 5px;
            border: 1px solid #aaaaaa;
        }
        .orange_btn{
            font-weight: 600;
            font-size: 15px;
            border-radius: 3px;
            padding: 15px 35px;
        }
        .baner_credits{
            font-size: 14px;
            color: lighten($main_text_color, 20%);
        }
    }

}

// Photos
.img_container{
    width: 25%;
    img{
        width: 100%;
    }
}
</style>

