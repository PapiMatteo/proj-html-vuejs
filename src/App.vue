<script>
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader
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
  </div>
  
</template>

<style lang="scss">
@use './style/general.scss';
@import '@fortawesome/fontawesome-free/css/all.css';

.header-section {
  background-image: url('./assets/img/home-background-hero-scaled.jpg');
  background-size: cover;
  min-height: 850px;
}

</style>
