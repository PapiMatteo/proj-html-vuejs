<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppHero,
    AppMain,
    AppFooter
},
  data() {
    return {
      headerNav: [
        'Home',
        'Order Online',
        'About',
        'News',
        'Contact Us'
      ],
      footerNav: [
        {
          title:'ORDER ONLINE',
          navigation: [
            'Appetizer',
            'Burgers',
            'Pizza',
            'Fries',
            'Sides',
            'Desserts',
            'Beverage',
            'Specials'
          ]
        },
        {
          title:'NAVIGATE',
          navigation: [
            'Home',
            'Alternate Home',
            'Menu',
            'About',
            'News',
            'Contact Us',
            'Cart'
          ]
        },
        {
          title:'INFORMATION',
          navigation: [
            'My Account',
            'Term Of Service',
            'Privacy Policy'
          ],
          imgList: [
            {
              imgPath: 'app-store-badge-200x67.png'
            },
            {
              imgPath: 'play-store-badge-200x67.png'
            }
          ]
        },
        {
          title:'OPENING HOURS',
          navigation: [
            {
              day: 'Mon -',
              hour: ' 10AM to 11PM'
            },
            {
              day: 'Tue -',
              hour: ' 10AM to 11PM'
            },
            {
              day: 'Wed -',
              hour: ' 10AM to 11PM'
            },
            {
              day: 'Thur -',
              hour: ' 10AM to 11PM'
            },
            {
              day: 'Fri -',
              hour: ' 10AM to 11PM'
            },
            {
              day: 'Sat -',
              hour: ' 10AM to 1AM'
            },
            {
              day: 'Sun -',
              hour: ' 11AM to 10PM'
            }
          ]
        },
        {
          title:'VOUCHER',
          imgList:[
            {
              imgPath: 'footer-coupon-200x200.png'
            }
          ]
          
        }
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
  <AppMain />
  <AppFooter :navItem="footerNav"/>
  
</template>

<style lang="scss">
@use './style/general.scss';
@import '@fortawesome/fontawesome-free/css/all.css';

.header-section {
  background-image: url('./assets/img/home-background-hero-scaled.jpg');
  background-size: cover;
  background-position: bottom;
  min-height: 700px;
}

</style>
