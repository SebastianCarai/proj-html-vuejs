<template>
    <header>
        <div class="container_65">
            <!-- Header socials -->
            <div class="d-flex justify-content-between my-3 header_links">
                <div>
                    <a href="#" class="mx-2 font_xs">Download app <span class="ios_btn">iOS</span></a>
                    <a href="#" class="mx-1 font_xs">Advertise with us</a>
                </div>
                <div>
                    <ul>
                        <li class="d-inline-block">
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="#"><i class="fab fa-instagram"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="#"><i class="fab fa-twitter"></i></a>
                        </li>
                        <li class="d-inline-block">
                            <a href="#"><i class="fab fa-youtube"></i></a>
                        </li>
                    </ul>
                </div>
            </div>

            <!-- Logo and Menu -->
            <div class="d-flex justify-content-center align-items-center m-5">
                <div>
                    <img src="../assets/img/avada-food-logo.png" alt="">
                    <ul class="header_menu">
                        <li v-for="(li, index) in headerUl" :key="index" class="my-5 mx-4 main_text_color" :class="{active: li.isActive}"> <a href="#">{{li.text}}</a> </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function(){
        return{
            headerUl: [
                {
                    text: 'Home',
                    isActive: true
                },
                {
                    text: 'Recipes',
                    isActive: false
                },
                {
                    text: 'Places',
                    isActive: false
                },
                {
                    text: 'Blog',
                    isActive: false
                },
                {
                    text: 'About',
                    isActive: false
                },
                {
                    text: 'Contact',
                    isActive: false
                }
            ]
        }   
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.header_links{
    color: #6a6b6c;
    .ios_btn{
        font-size: 7px;
        padding: 3px 8px;
        background-color: $main_color;
        color: white;
        border-radius: 5px;
    }
    i{
        color: #9c9894;
        margin: 0 15px;
    }
}
img{
    display: block;
    margin: auto;
}
.header_menu{
    line-height: 40px;
    li{
        display: inline-block;
        font-weight: 600;
        &.active{
            color: $main_color;
            border-bottom: 4px solid $main_color;
        }
    }
}

</style>