<template>
  <div class="box-title d-flex justify-content-center align-items-center flex-column">
     <p class="title">{{voiceTitle.title}}</p>
     <div class="line"></div>
     <p class="subtitle">{{voiceTitle.subtitle}}</p>
  </div>
</template>

<script>
export default {
name: "TitleSection",
  props: {
    voiceTitle: Object,
  },
}
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.box-title{
   padding-top: 60px;
   margin-top: 80px;
   .title{
      padding: 5px 0;
   }
   .line{
      display: block;
      height: 2px;
      width: 200px;
      background-color: $second-color;
   }
   .subtitle{
      padding: 32px 0; 
      width: 800px;
      text-align: center;
      }
}

</style>