<template>
  <main>
    <Jumbotron />
    <TitleSection :voiceTitle="this.VoiceTitle[0]"/>
    <OptionConstruction/>
    <JumboConstruction/>
    <TitleSection :voiceTitle="this.VoiceTitle[1]"/>

  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import JumboConstruction from "./JumboConstruction"
import OptionConstruction from './OptionConstruction.vue'
import TitleSection from './TitleSection.vue'
import VoiceTitle from "../assets/data/title-section.js";

export default {
  name: "Main",
  components: {
    Jumbotron,
    TitleSection,
    OptionConstruction,
    JumboConstruction,
  },
  // props: {
  //   filmsList: Array,
  //   seriesList: Array,
  // },
   data(){
     return{
       VoiceTitle,
     }
   },
  // methods:{
  //   runLeftMovie(){
  //     this.pxTraslMovie = this.pxTraslMovie - 450;
  //     console.log('Movie',this.pxTraslMovie);
  //   },
  //   runRightMovie(){
  //     this.pxTraslMovie = this.pxTraslMovie + 450;
  //     console.log('Movie', this.pxTraslMovie);
  //   },
  //   runLeftTv(){
  //     this.pxTraslTv = this.pxTraslTv - 450;
  //     console.log('Tv',this.pxTraslTv);
  //   },
  //   runRightTv(){
  //     this.pxTraslTv = this.pxTraslTv + 450;
  //     console.log('Tv', this.pxTraslTv);
  //   },

  // },
};
</script>

<style lang="scss">
main {
  height: 100vh;
}
</style>
