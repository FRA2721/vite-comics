<!-- script-section -->
<script>
export default{
    // name
    name: "AppComicsList"
}
</script>
<!-- /script-section -->

<!-- template-section -->
<template>

    <!-- comics-section -->
    <section class="comics">

        <!-- comics-section-container -->
        <div class="container">

            <!-- comics-list-section -->
            <div class="comics-list">
                <h2>FRANCESCO CIMINO... Cooming soon...</h2>
            </div>
            <!-- /comics-list-section -->

        </div>
        <!-- /comics-section-container -->

    </section>
    <!-- /comics-section -->
</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.comics{
    background-color: $secondary;
    .container{
        color: white;
        .comics-list{
            margin-top: 30px;
            padding: 3em 0;
        }

        h2{
            transition-duration: 1s;
        }

        &:hover{
            color: red;
            cursor: pointer;
        }
    }
}
</style>
<!-- /style-section -->