<!-- script-section -->
<script>
export default{
    // name
    name: "ProductList"
}
</script>
<!-- /script-section -->

<!-- template-section -->
<template>

    <!-- products-section -->
    <section class="products">

        <!-- products-section-container -->
        <div class="container">

            <!-- products-list-section -->
            <div class="products-list">
                <h2>FRANCESCO CIMINO... Coming soon...</h2>
            </div>
            <!-- /products-list-section -->

        </div>
        <!-- /products-section-container -->

    </section>
    <!-- /products-section -->
</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.products{
    background-color: $secondary;
    .container{
        color: white;
        .products-list{
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