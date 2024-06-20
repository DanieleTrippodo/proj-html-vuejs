<script >
import Jumbotron from './components/Jumbotron.vue'; /* Ricordatevi di importare i vostri componenti, una volta finiti */
import MainFooter from './components/MainFooter.vue';
import AlbumOutNow from './components/AlbumOutNow.vue';
import SenseTheJazz from './components/SenseTheJazz.vue';
import AppHeader from './components/AppHeader.vue';
import NewMusicVideo from './components/NewMusicVideo.vue';
import JumboCards from './components/JumboCards.vue';
import Statistics from './components/Statistics.vue';
import CardContainer from './components/CardContainer.vue';
import BottomSlider from './components/BottomSlider.vue';
import "@fontsource/oswald";


export default {
  name: 'App',
  components: {
    AppHeader,
    Jumbotron,
    SenseTheJazz,
    NewMusicVideo,
    AlbumOutNow,
    MainFooter,
    JumboCards,
    Statistics,
    CardContainer,
    BottomSlider
  }
};
</script>

<template>
  <!-- Contenuto HTML -->

<!-- Header ---------------- -->
  <AppHeader/>
<!-- Header ---------------- -->
  


  <Jumbotron/>

  <JumboCards/>

  <SenseTheJazz/>

  <AppNewMusic/>
  <CardContainer/>
  <AlbumOutNow/>
  <Statistics/>
  <BottomSlider/>
  <!-- Footer ---------------- -->
  <MainFooter/>
  <!-- Footer ---------------- -->


</template>

<style lang="scss">
@use "./main.scss";
</style>
