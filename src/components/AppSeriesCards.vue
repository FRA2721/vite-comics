<!-- script-section -->
<script>
export default{
    name: "AppSeriesCard",
    props: {
        imgUrl: String, nameSeries: String, seriesPrice: String
    }
}
</script>
<!-- /script-section -->

<!-- template-section -->
<template>
    <div class="series">
        <img :src="imgUrl" alt="series images">
        <h3>{{ nameSeries }}</h3>
        <h4>{{ seriesPrice }}</h4>
    </div>
</template>
<!-- /template-section -->

<!-- style-section -->
<style lang="scss" scoped>

// mixin-&-variables
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// series-formatting-section
.series{
    margin: .5em;
    width: calc(100% / 6 - 3em);
    padding-bottom: 3rem;

    // img-formatting-section
    img{
        object-position: top;
        object-fit: cover;
        width: 100%;
        height: 100%;
        padding: 1rem;
        transition-duration: 1s;
        margin-left: 100px;
        margin-top: 30px;
        opacity: .5;
        border: 3px solid white;

        &:hover{
            transform: scale(.95);
            border-radius: 33px;
            cursor: pointer;
            opacity: 1;
            border: 3px solid $primary;
        }
    }

    // h3-tipography
    h3{
        width: 150px;
        color: white;
        margin-left: 120px;
        font-size: .8rem;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    h4{
        width: 150px;
        color: grey;
        // text-align: center;
        margin-left: 120px;
        font-size: .8rem;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
}
</style>
<!-- /style-section -->