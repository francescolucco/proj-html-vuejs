<template>
  <div class="container">
    <CardCoreValues />
  </div>
</template>

<script>
import CardCoreValues from "./CardCoreValues.vue";

export default {
  name: "OurCoreValues",
  components: {
    CardCoreValues,
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
.box{
  padding: 0 150px;
}
</style>