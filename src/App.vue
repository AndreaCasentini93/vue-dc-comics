<template>
  <div id="app">
    <!-- HEADER -->
    <Header />
    <!-- /HEADER -->

    <!-- MAIN -->
    <main>
      <div class="container debug">
        Content goes here
      </div>
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
import BlueMenu from './components/BlueMenu.vue';
import FooterLinks from './components/FooterLinks.vue';
import FooterSocial from './components/FooterSocial.vue';

export default {
  name: 'App',
  components: {
    Header,
    BlueMenu,
    FooterLinks,
    FooterSocial
  }
}
</script>

<style lang="scss">
  @import './style/general.scss';

  // Debug
  main {
    background-color: #000000;
    .container.debug {
      padding: 50px 0;
      font-size: 25px;
      font-weight: 700;
      color: #FFFFFF;
    }
  }
  // /Debug
</style>
