<!-- dev: Francesco Cimino; -->
<!-- proj: Vite DC Comics; -->



<!-- script-section -->
<script>

// import-AppHeader.vue
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import AppIcons from './components/AppIcons.vue';

export default{

  // components
  components: {
    AppHeader, 
    ProductList,
    AppIcons
  }
}
</script>
<!-- /script-section -->



<!-- template-section -->
<template>

  <!-- header-section -->
  <header>
    <AppHeader />
  </header>  
  <!-- /header-section -->

  <!-- main-section -->
  <main>
    <ProductList />
    <AppIcons />
  </main>
  <!-- /main-section -->

</template>
<!-- /template-section -->



<!-- style-section -->
<style lang="scss">

// use-scss
@use "./styles/general.scss" as *;

</style>
<!-- /style-section -->