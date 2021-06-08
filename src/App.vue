<template>
  <div id="app">
    <!-- HEADER -->
    <Header />
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
  }
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
