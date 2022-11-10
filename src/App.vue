<!-- dev: Francesco Cimino; -->
<!-- proj: Vite DC Comics; -->



<!-- script-section -->
<script>

// importing-section-vue-file
import AppHeader from './components/AppHeader.vue';
import AppComicsList from './components/AppComincsList.vue';
import AppBannerIcons from './components/AppBannerIcons.vue';
import AppFooterHref from './components/AppFooterHref.vue';
import AppFooterSocialHref from './components/AppFooterSocialHref.vue';

export default{

  // components
  components: {
    AppHeader, AppComicsList, AppBannerIcons, AppFooterHref, AppFooterSocialHref
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
    <AppComicsList />
    <AppBannerIcons />
  </main>
  <!-- /main-section -->

  <!-- footer-section -->
  <footer>
    <AppFooterHref />
    <AppFooterSocialHref />
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