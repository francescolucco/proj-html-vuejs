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
      <JumboSpaces />
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
import JumboSpaces from "./JumboSpaces.vue";
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
    JumboSpaces,
  },
  data() {
    return {
      VoiceTitle,
    };
  },
};
</script>

<style lang="scss">
main {
  .back-grey {
    background-color: #f5f5f5;
  }
}
</style>
