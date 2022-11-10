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
import AppJumbotron from './components/AppJumbotron.vue';

export default{

  // components
  components: {
    AppHeader, AppJumbotron, AppComicsList, AppBannerIcons, AppFooterHref, AppFooterSocialHref
  },
  methods: {
    getImagePath(imgPath){
      return new URL(imgPath, import.meta.url).href;
    }

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
    <AppJumbotron :imgUrl="getImagePath('./assets/img/jumbotron.jpg')" :text="'CURRENT SERIES'" />
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