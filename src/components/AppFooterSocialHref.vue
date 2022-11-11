<!-- script-section -->
<script>
export default{
    // name
    name: "AppFooterSocialHref",
    data(){
        return {
            socialHref: [
                {
                    name: "facebook", href: "/facebook", imgUrl: "../assets/img/footer-facebook.png"
                },

                {
                    name: "twitter",  href: "/twitter", imgUrl: "../assets/img/footer-twitter.png"
                },  

                {
                    name: "youtube", href: "/youtube", imgUrl: "../assets/img/footer-youtube.png"
                },   

                {
                    name: "pinterest", href: "/pinterest", imgUrl: "../assets/img/footer-pinterest.png"
                },

                {
                    name: "periscope", href: "/periscope", imgUrl: "../assets/img/footer-periscope.png"
                }
            ]
        }
    },
    methods: {
        getImagePath(imgPath){
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>
<!-- /script-section -->

<!-- template-section -->
<template>

    <!-- socail-section -->
    <div class="social">

        <!-- social-container -->
        <div class="social-container">

            <!-- button -->
            <div class="button">
                <button>SIGN-UP NOW!</button>
            </div>
            <!-- /button -->

            <!-- social-logo -->
            <div class="social-links">
                <h3>FOLLOW US</h3>
                <ul>

                    <!-- list-logo -->
                    <li v-for="(social,index) in socialHref" :key="index">
                        <a :href="social.href">
                            <img :src="getImagePath(social.imgUrl)" :alt="social.name">
                        </a>
                    </li>
                    <!-- /list-logo -->

                </ul>
            </div>
            <!-- /social-logo -->

        </div>
        <!-- /social-container -->

    </div>
    <!-- /social-section -->
</template>
<!-- /template-section -->

<!-- style-section -->
<style lang="scss" scoped>

// mixin-&-variables
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// social
.social{
    background-color: $tertiary;
    border-top: 3px solid grey;
    border-bottom: 3px solid grey;
    .social-container{
        justify-content: space-between;
        padding: 3em 5em;
        @include flex-center("vertical");

        // button-formatting-section
        .button{
            button{
                padding: 1em;
                color: white;
                border-radius: 50px;
                border: 3px solid $primary;
                background-color: $tertiary;
                transition-duration: 1s;

                &:hover{
                    cursor: pointer;
                    color: $primary;
                    border:3px solid white;
                    transform: scale(0.9);
                }
            }
        }

        // social-links-formatting-section
        .social-links{
            @include flex-center("vertical");

            // h3-tipography
            h3{
                color: $primary;
            }

            // social-logo-formatting-section
            ul{
                margin: 0 3em;
                @include flex-center("vertical");

                li{
                    margin: 0 .3em;
                    transition-duration: .5s;

                    &:hover{
                        transform: scale(1.1);
                    }
                }
            }
        }
    }
}
</style>
<!-- /style-section -->