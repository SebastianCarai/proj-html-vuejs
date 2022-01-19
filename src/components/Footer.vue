<template>
    <footer>
        <div class="container">
            <div class="d-flex">

                <!-- Footer socials -->
                <div class="footer_col">
                    <img src="../assets/img/avada-food-logo-mob.png" class="footer_logo" alt="Logo">
                    <SocialLinks class="mt-5"/>
                </div>

                <!-- Links -->
                <div class="footer_col mid_col">
                    <ul>
                        <li v-for="(singleLink, index) in footerLinks" :key="index">
                            <a :href="singleLink.link"> {{ singleLink.text }} </a>
                        </li>
                    </ul>
                </div>

                <!-- Contacts -->
                <div class="footer_col mid_col">
                    <div class="contacts_container">
                        <h3 class="footer_title">CONTACT</h3>

                        <ul>
                            <li>
                                <i class="fas fa-map-marker-alt"></i> <span>775 New York Ave, Brooklyn, Kings, New York 11203</span>
                            </li>
                            <li>
                                <i class="fas fa-phone"></i> <span>+ 0100-505-0000</span>
                            </li>
                            <li>
                                <i class="fas fa-envelope"></i> <span>info@your-domain.com</span>
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- Get App -->
                <div class="footer_col">
                    <div>
                        <h3 class="footer_title mx-3">GET APP</h3>

                        <!-- GooglePlay link -->
                        <div class="app_link my-4 d-flex align-items-center">
                            <div>
                                <i class="fas fa-play"></i>
                            </div>

                            <div class="mx-3">
                                <div>
                                    GET IT ON
                                </div>
                                <div class="where">
                                    Google Play
                                </div>
                            </div>
                        </div>

                        <!-- AppStore link -->
                        <div class="app_link d-flex align-items-center">
                            <div>
                                <i class="fab fa-apple"></i>
                            </div>

                            <div class="mx-3">
                                <div>
                                    GET IT ON
                                </div>
                                <div class="where">
                                    App Store
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import SocialLinks from './SocialLinks.vue'

export default {
    name: 'Footer',
    components:{
        SocialLinks
    },
    data: function(){
        return{
            footerLinks:[
                {
                    text: 'Recipes',
                    link: '#'
                },
                {
                    text: 'Places',
                    link: '#'
                },
                {
                    text: 'Blog',
                    link: '#'
                },
                {
                    text: 'About',
                    link: '#'
                },
                {
                    text: 'Contact',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

footer{
    padding: 100px 0;
    &  div.d-flex{
        width: 90%;
        margin: auto;
    }
    .footer_col{
        width: 25%;
        .footer_title{
            color: $main_color;
            font-size: 16px;
        }
        .footer_logo{
            width: 90%;
        }
        &.mid_col{
            border-left: 1px solid #e0dede;
            border-right: 1px solid #e0dede;
            // Links
            li{
                margin: 0 0 20px 30px;
                a{
                    font-size: 18px;
                    font-weight: 600;
                    color: $main_text_color;
                }
            }
        }
        // Contacts & Get app
        .contacts_container{
            width: 85%;
            margin: auto;
            li{
                color: lighten($main_text_color, 30%);
                margin: 0 0 20px 0;
                font-size: 20px;
                span{
                    font-size: 17px;
                    margin-left: 10px;
                }
            }
        }

        // App links
        .app_link{
            padding: 10px;
            border: 2px solid #67615a;
            border-radius: 10px;
            color: #67615a;
            i{
                font-size: 40px;
                &.fa-apple{
                    font-size: 50px;
                }
            }
            .where{
                font-size: 30px;
            }
        }
    }
}

</style>