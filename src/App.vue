<template>
  <div>
    <Header @titleSearch="titleToSendApi" 
    @returnHome="this.getApipopular('movie')"/>
    <Main :filmsList="movie" :seriesList="tv" />
  </div>
</template>

<script>
import Header from "./components/Header";
import Main from "./components/Main";

export default {
  name: "App",
  data() {
    return {

    };
  },
  components: {
    Header,
    Main,
  },
  methods: {

  },
    mounted() {

    },

};
</script>

<style lang="scss">
@import './assets/styles/vars.scss';
@import './assets/styles/mixin.scss';
@import './assets/styles/generals.scss';
@import './assets/styles/utilities.scss';
</style>

