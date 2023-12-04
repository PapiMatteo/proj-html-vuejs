<script>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue'

export default {
  components: {
    AppHeader,
    AppHero
  },
  data() {
    return {
      headerNav: [
        'Home',
        'Order Online',
        'About',
        'News',
        'Contact Us'
      ]
    }
  }
}
</script>

<template>
  <div class="header-section">
    <AppHeader :navItems="headerNav"/>
    <AppHero />
  </div>
  
</template>

<style lang="scss">
@use './style/general.scss';
@import '@fortawesome/fontawesome-free/css/all.css';

.header-section {
  background-image: url('./assets/img/home-background-hero-scaled.jpg');
  background-size: cover;
  min-height: 700px;
}

</style>
