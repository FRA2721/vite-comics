<!-- script-section -->
<script>
export default{
    // name
    name: "FooterLinks",
    data(){
        return {
            footerHrefArray: [
                {
                    // dc-comics-section
                    text: "dc comics",
                    links: [
                        {
                            text: "Characters", href: "/characters"
                        },

                        {
                            text: "Comics", href: "/comics"
                        },

                        {
                            text: "Movies", href: "/movies"
                        },

                        {
                            text: "Tv", href: "/tv"
                        },

                        {
                            text: "Games", href: "/games"
                        },

                        {
                            text: "Videos", href: "/videos"
                        },

                        {
                            text: "News", href: "/news"
                        },
                    ]
                },

                {
                    // dec-section
                    text: "dc",
                    links: [
                        {
                            text: "Terms Of Use", href: "/terms-of-use"
                        },

                        {
                            text: "Privacy policy (New)", href: "/privacy-policy-new"
                        },

                        {
                            text: "Ad Choise", href: "/ad-choise"
                        },

                        {
                            text: "Advertising", href: "/advertising"
                        },

                        {
                            text: "Jobs", href: "/jobs"
                        },

                        {
                            text: "Subscriptions", href: "/subscriptions"
                        },

                        {
                            text: "Talent Workshops", href: "/talent-workshops"
                        },

                        {
                            text: "CPSC Certificates", href:"/cpsc-certificates"
                        },

                        {
                            text: "Ratings", href:"/ratings"
                        },

                        {
                            text: "Shop Help", href:"/shop-help"
                        },

                        {
                            text:"Contact Us", href:"/contact-us"
                        }
                    ]
                },

                {
                    // sites-section
                    text: "sites",
                    links: [
                        {
                            text:"DC", href:"dc"
                        },

                        {
                            text:"MAD Magazine", href:"/mad-magazine"
                        },

                        {
                            text:"DC Kids", href:"/dc-kids"
                        },

                        {
                            text:"DC Universe", href:"/DC Power Visa"
                        },

                        {
                            text:"DC Power Visa", href:"/dc-power-visa"
                        }

                    ]
                },

                {
                    // shop-section
                    text: "shop",
                    links: [
                        {
                            text: "Shop DC", href: "/shopdc"
                        },

                        {
                            text: "Shop DC Collectibles", href: "/shopdcCollectibles"
                        },
                    ]
                },
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

    <!-- footer-href-section -->
    <div class="footer-href">

        <!-- footer-container -->
        <div class="container">
            <div class="footer-href-array">

                <ul v-for="(category, index) in footerHrefArray" :key="index">
                    <h3>{{ category.text.toUpperCase() }}</h3>
                    <li v-for="(link, secondaryIndex) in category.links" :key="secondaryIndex"><a :href="link.href">{{ link.text }}</a></li>
                </ul>

            </div>

            <!-- background-image -->
            <div class="background-img">
                <img src="../assets/img/dc-logo-bg.png" alt="background image">
            </div>
            <!-- /background-image -->

        </div>
        <!-- /footer-container -->

    </div>
    <!-- /footer-href-section -->
</template>
<!-- /template-section -->

<!-- style-section -->
<style lang="scss" scoped>

// mixin-&-variables
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// footer-section-formatting
.footer-href{
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    background-repeat: no-repeat;

    // footer-container
    .container {
        display: flex;
        overflow: hidden;
        position: relative;

        // array-formatting
        .footer-href-array{
            width: 50%;
            display: flex;
            flex-wrap: wrap;
            padding: 5em 0;

            // list-href-formatting
            ul{
                margin: 0 .6em;
                width: calc(100% / 4 - .5em);

                // list-items-href
                li{
                    margin: .3em 0;

                    a{
                        color: grey;
                        font-size: .9rem;
                    }

                }

                // toCheck
                // a:hover{
                //     cursor: pointer;
                //     color: $primary;
                // }
                
                // h3-tipography
                h3{
                    font-size: 1.5rem;
                    color: white;
                    margin-bottom: 1rem;
                }
            }
        }

        // background-image
        .background-img{
            display: flex;
            width: 100%;
            position: absolute;
            right: 0;
            top: 50%;
            justify-content: flex-end;
            transform: translateY(-50%);
        }
    }
}
</style>
<!-- /style-section -->