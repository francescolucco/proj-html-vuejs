<template>
  <div class="box">
    <CardConstruction />
  </div>
</template>

<script>
import CardConstruction from "./CardConstruction.vue";
// import dataCardConstruction from "../assets/data/card-construction.js";

export default {
  name: "OptionConstruction",
  components: {
    CardConstruction,
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
.box{
  padding: 0 150px;
}
</style>
