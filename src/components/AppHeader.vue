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
                    name: "characters",
                    href: "/characters",
                    active: false,
                },

                {
                    name: "comics",
                    href: "/comics",
                    active: true,
                },  

                {
                    name: "movies",
                    href: "/movies",
                    active: false,
                },

                {
                    name: "tv",
                    href: "/tv",
                    active: false,
                },
                {

                    name: "games",
                    href: "/games",
                    active: false,
                },

                {
                    name: "collectibles",
                    href: "/collectibles",
                    active: false,
                },

                {
                    name: "videos",
                    href: "/videos",
                    active: false,
                },

                {
                    name: "fans",
                    href: "/fans",
                    active: false,
                },

                {
                    name: "news",
                    href: "/news",
                    active: false,
                },

                {
                    name: "shop",
                    href: "/shop",
                    active: false,
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
        margin-left: 60px;
        margin-top: 33px;
        @include flex-center("vertical");
    }

    // nav-section
    .nav{
        width: 50%;

        // nav-array-nav-formatting-section
        ul{
            height: 100%;
            margin-right: 200px;
            // mixin
            @include flex-center("horizontal");

            // items-formatting
            li {
                height: 100%;
                margin: .4em;
                // mixin
                @include flex-center("vertical");

                // anchor-formatting
                a{
                    color: black;
                    font-size: .6rem;
                    text-decoration: none;
                    transition-duration: 1s;
                }
                
                // &:hover{
                // }
                &.active{
                    border-bottom: 1.5px solid $primary;
                    border-radius: 3px;
                }
                
            }
        }
    }
}
</style>
<!-- /style-section -->