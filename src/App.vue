<template>
  <div id="app">
    <!-- HEADER -->
    <Header :links="menu"/>
    <!-- /HEADER -->

    <!-- MAIN -->
    <main>
      <Jumbotron />
      <DcVolumes />
      <BlueMenu />
    </main>
    <!-- /MAIN -->

    <!-- FOOTER -->
    <footer>
      <FooterLinks />
      <FooterSocial />
    </footer>
    <!-- /FOOTER -->
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import DcVolumes from './components/DcVolumes.vue';
import BlueMenu from './components/BlueMenu.vue';
import FooterLinks from './components/FooterLinks.vue';
import FooterSocial from './components/FooterSocial.vue';

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    DcVolumes,
    BlueMenu,
    FooterLinks,
    FooterSocial
  },
  data: function() {
    return {
      menu: [
        {
            text: 'Characters',
            url: '#',
            current: false
        },
        {
            text: 'Comics',
            url: '#',
            current: true
        },
        {
            text: 'Movies',
            url: '#',
            current: false
        },
        {
            text: 'TV',
            url: '#',
            current: false
        },
        {
            text: 'Games',
            url: '#',
            current: false
        },
        {
            text: 'Collectibles',
            url: '#',
            current: false
        },
        {
            text: 'Videos',
            url: '#',
            current: false
        },
        {
            text: 'Fans',
            url: '#',
            current: false
        },
        {
            text: 'News',
            url: '#',
            current: false
        },
        {
            text: 'Shop',
            url: '#',
            current: false
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
