<template>
  <main>
    <Jumbotron />
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
export default {
  name: "Main",
  components: {
    Jumbotron,
  },
  // props: {
  //   filmsList: Array,
  //   seriesList: Array,
  // },
  //  data(){
  //    return{
  //      Cards,
  //    }
  //  },
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
  background-color: black;
  height: 100vh;
}
</style>
