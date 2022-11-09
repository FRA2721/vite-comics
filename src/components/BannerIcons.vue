<!-- script-section -->
<script>

export default{
    // text
    text: "BannerIcons",

    data(){
        return {
            bannerLinksArray: [
                {
                    text: "digital comics",
                    href: "/digital-comics",
                    imgUrl: "../assets/img/buy-comics-digital-comics.png"
                },

                {
                    text: "dc merchandise",
                    href: "/dc-merchandise",
                    imgUrl: "../assets/img/buy-comics-merchandise.png"
                },

                {
                    text: "subscription",
                    href: "/subscription",
                    imgUrl: "../assets/img/buy-comics-subscriptions.png"
                },

                {
                    text: "comic shop locator",
                    href: "/comic-shop-locator",
                    imgUrl: "../assets/img/buy-comics-shop-locator.png"
                },

                {
                    text: "dc power visa",
                    href: "/dc-power-visa",
                    imgUrl: "../assets/img/buy-dc-power-visa.svg"
                },
            ]
        }
    },

    // getImagePath-method(imgs/sections)
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

    <!-- banner/section -->
    <section class="banner">

        <!-- banner/container -->
        <div class="container">
            <ul>
                <li v-for="(link,index) in bannerLinksArray" :key="index">
                    <!-- imags-src -->
                    <img :src="getImagePath(link.imgUrl)" :alt="link.text">
                    <a href="">{{link.text.toUpperCase()}}</a>
                </li>
            </ul>
        </div>
        <!-- /banner/contaier -->
    </section>
    <!-- /banner/section -->

</template>
<!-- /template-section -->

<!-- style-section -->
<style lang="scss" scoped>
// mixin-&-variables
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.banner{
    color: white;
    background-color: $primary;

    // container
    .container{
        padding: 3em 0;

        // list
        ul{
            display: flex;
            justify-content: space-around;

            li{
                @include flex-center;
                // anchor
                a{
                    color: white;
                    padding: 0 .5em;
                    font-size: .7rem;
                }

                // img
                img{
                    width: 33px;
                }

            }
        }
    }
}
</style>
<!-- /style-section -->