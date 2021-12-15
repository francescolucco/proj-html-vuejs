<template>
  <div class="container">
    <div class="row">
      <div v-for="(item, index) in Images" :key="index" class="col logo-partners">
        <img :src="require(`../assets/img/${item.img}`)" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
import Images from "../assets/data/logo-partners.js";
export default {
  name: "Partners",
  data() {
    return {
      Images,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";

.row{
   padding: 0 0 145px 0;
}
.logo-partners{
   height: 100px;
   margin: 18px;
   img{
      width: 100%;
   }
}
</style>
