<template>
  <main>
    <Jumbotron />
    <TitleSection :voiceTitle="this.VoiceTitle[0]" />
    <OptionConstruction />
    <JumboConstruction />
    <TitleSection :voiceTitle="this.VoiceTitle[1]" />
    <ResentWork />
    <div class="back-grey">
      <TitleSection :voiceTitle="this.VoiceTitle[2]" />
      <OurCoreValues />
      <JumboOwnersSay />
      <TitleSection :voiceTitle="this.VoiceTitle[4]" />
      <LatestNews />
    </div>
      <TitleSection :voiceTitle="this.VoiceTitle[5]" />
      <Partners />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import OurCoreValues from "./OurCoreValues.vue";
import JumboOwnersSay from "./JumboOwnersSay.vue";
import JumboConstruction from "./JumboConstruction";
import ResentWork from "./ResentWork";
import LatestNews from "./LatestNews";
import Partners from "./Partners";
import OptionConstruction from "./OptionConstruction.vue";
import TitleSection from "./TitleSection.vue";
import VoiceTitle from "../assets/data/title-section.js";

export default {
  name: "Main",
  components: {
    Jumbotron,
    TitleSection,
    OptionConstruction,
    JumboConstruction,
    ResentWork,
    OurCoreValues,
    JumboOwnersSay,
    LatestNews,
    Partners,
  },
  // props: {
  //   filmsList: Array,
  //   seriesList: Array,
  // },
  data() {
    return {
      VoiceTitle,
    };
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
  .back-grey {
    background-color: #f5f5f5;
  }
}
</style>
