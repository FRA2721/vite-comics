<!-- script-section -->
<script>
export default{
    // name-&-props
    name: "AppJumbotron",
    props: {
        imgUrl: String, text: String
    }
}
</script>
<!-- /script-section -->

<!-- tempalte-section -->
<template>

    <!-- jumbotron-section -->
    <div class="jumbotron">
        <img :src="imgUrl" alt="jumbo photo">

        <!-- jumbotron-container -->
        <div class="jumbotron-container">
            <div class="jumbo-section">
                <h3>{{ text }}</h3>
            </div>
        </div>
        <!-- /jumbotron-container -->

    </div>
    <!-- /jumbotron-section -->
</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss" scoped>

// variables
@use "../styles/partials/variables" as *;

// jumbotron-formatting-section
.jumbotron{
    margin-top: 50px;
    width: 100%;
    height: 333px;

    // img-formatting-section
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
        transition-duration: 1s;
        opacity: .5;
        border-top: 3px solid fuchsia;
        border-bottom: 3px solid fuchsia;

        &:hover{
            opacity: 1;
        }
    }

    // jumbotron-formatting-container-section
    .jumbotron-container{
    position: relative;        
        .jumbo-section{
            position: absolute;
            top: 50%;
            left: 108px;
            padding: .5em 3em;
            color: white;
            transform: translateY(-50%);
            background-color: $primary;
            border: 3px solid white;
        }
    }
}
</style>
<!-- /style-section -->