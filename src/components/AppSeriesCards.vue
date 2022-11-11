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
        <p>{{ nameSeries }}</p>
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
    transition-duration: 1s;

    
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
    
    &:hover p{
        color: $primary;
    }

    // p-tipography
    p{
        width: 150px;
        color: white;
        margin-left: 100px;
        font-size: .8rem;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    h4{
        width: 150px;
        color: grey;
        // text-align: center;
        margin-left: 100px;
        font-size: .8rem;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
}
</style>
<!-- /style-section -->