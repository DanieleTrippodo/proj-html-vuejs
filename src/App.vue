<script >
import Jumbotron from './components/Jumbotron.vue'; /* Ricordatevi di importare i vostri componenti, una volta finiti */
import MainFooter from './components/MainFooter.vue';
import AlbumOutNow from './components/AlbumOutNow.vue';
import SenseTheJazz from './components/SenseTheJazz.vue';
import AppHeader from './components/AppHeader.vue';
import NewMusicVideo from './components/NewMusicVideo.vue';
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
    Statistics,
    CardContainer,
    BottomSlider
  }
};

console.log('work organization dev https://www.figma.com/design/Oxc3MyvNepMNJntHDVmfh9/Figma-basics?node-id=1669-162202&t=a50dx6WNCl1FAAyL-1');
</script>

<template>
  <!-- Contenuto HTML -->

<!-- Header ---------------- -->
  <AppHeader/>
<!-- Header ---------------- -->
  


  <Jumbotron/>


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
