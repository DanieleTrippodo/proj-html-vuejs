<script >
import Jumbotron from './components/Jumbotron.vue'; /* Ricordatevi di importare i vostri componenti, una volta finiti */
import MainFooter from './components/MainFooter.vue';
import AlbumOutNow from './components/AlbumOutNow.vue';
import SenseTheJazz from './components/SenseTheJazz.vue';
import AppHeader from './components/AppHeader.vue';
import AppNewMusic from './components/NewMusicVideo.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    Jumbotron,
    SenseTheJazz,
    AppNewMusic,
    AlbumOutNow,
    MainFooter
  }
};
</script>

<template>
  <!-- Contenuto HTML -->

<!-- Header ---------------- -->
  <AppHeader/>
<!-- Header ---------------- -->
  


  <Jumbotron/>

  <SenseTheJazz/>

  <AppNewMusic/>

  <AlbumOutNow/>


  <!-- Footer ---------------- -->
  <MainFooter/>
  <!-- Footer ---------------- -->


</template>

<style lang="scss" scoped>

</style>
