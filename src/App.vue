<!-- dev: Francesco Cimino; -->
<!-- proj: Vite DC Comics; -->



<!-- script-section -->
<script>

// impoerting-section-vue-file
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import BannerIcons from './components/BannerIcons.vue';
import FooterLinks from './components/FooterLinks.vue';

export default{

  // components
  components: {
    AppHeader, ProductList, BannerIcons, FooterLinks
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
    <BannerIcons />
  </main>
  <!-- /main-section -->

  <!-- footer-section -->
  <footer>
    <FooterLinks />
  </footer>
  <!-- /footer-section -->

</template>
<!-- /template-section -->



<!-- style-section -->
<style lang="scss">

// use-scss
@use "./styles/general.scss" as *;

</style>
<!-- /style-section -->