<!-- script-section -->
<script>
export default{

    // name
    name: "AppHeader",
    data(){
        return {

            // set-array-nav
            navArray: [
                {
                    name: "characters", href: "/characters"
                },

                {
                    name: "comics", href: "/comics"
                },  

                {
                    name: "movies", href: "/movies"
                },

                {
                    name: "tv", href: "/tv",
                },
                {

                    name: "games", href: "/games"
                },

                {
                    name: "collectibles", href: "/collectibles"
                },

                {
                    name: "videos", href: "/videos"
                },

                {
                    name: "fans", href: "/fans"
                },

                {
                    name: "news", href: "/news"
                },

                {
                    name: "shop", href: "/shop"
                }
            ]
        }
    }
}
</script>
<!-- /script-section -->



<!-- template-section -->
<template>

    <!-- header-section -->
    <header>

        <!-- container -->
        <div class="container">

            <!-- logo-section -->
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="dc comics logo">
            </div>
            <!-- /logo-section -->

            <!-- nav-section -->
            <nav class="nav">
                <ul>
                    <li v-for="link in navArray" :class="{'active' : link.active}">
                        <a :href="link.href">{{ link.name.toUpperCase() }}</a>
                    </li>
                </ul>
            </nav>
            <!-- /nav-section -->

        </div>
        <!-- /container -->

    </header>
    <!-- /header-section -->

</template>
<!-- /template-section -->



<!-- style-section -->
<style lang="scss" scoped>

// mixins-&-variables
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// header
header {
    // container
    .container{
        @include flex-center("horizontal");
    }

    // logo
    .logo{
        width: 100%;
        margin-right: 500px;
        margin-top: 33px;
        transition-duration: 1s;
        @include flex-center("horizontal");
    }

    .logo:hover{
        transform: scale(1.1);
        cursor: pointer;
    }
    // nav-section
    .nav{
        width: 50%;

        // nav-array-nav-formatting-section
        ul{
            height: 100%;
            margin-right: 200px;
            @include flex-center("horizontal");

            // items-formatting
            li {
                height: 100%;
                margin: 1em;
                transition-duration: .3s;
                @include flex-center("vertical");

                &:hover{
                    border-radius: 3px;
                    border-bottom: 5px solid $primary;
                    cursor: pointer;
                }
                // anchor-formatting
                a{
                    color: black;
                    font-size: 1rem;
                    text-decoration: none;
                    transition-duration: 1s;

                    &:hover{
                        color: $primary;
                    }
                }

            }
        }
    }
}
</style>
<!-- /style-section -->