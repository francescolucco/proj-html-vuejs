<template>
  <div class="app">
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Main from "./components/Main";
import Footer from "./components/Footer";

export default {
  name: "App",
  data() {
    return {

    };
  },
  components: {
    Header,
    Main,
    Footer,
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

.app{
  width: 100%;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>

