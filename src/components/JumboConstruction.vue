<template>
  <div class="section-img-curve">
     <div class="block-white-top"></div>
     <img src="../assets/img/home-244125289.jpg" alt="">
     <div class="block-white-bottom"></div>
     <div class="container d-flex justify-content-center align-items-center">
        <GoalsConstruction/>
     </div>
  </div>
</template>

<script>
import GoalsConstruction from './GoalsConstruction.vue'

export default {
name: 'JumboConstruction',
components:{
   GoalsConstruction
}
}
</script>

<style lang="scss">
.section-img-curve{
   margin: 100px 0;
   height: 600px;
   overflow: hidden;
   position: relative;
   .block-white-top{
      display: block;
      height: 100px;
      width: 100%;
      background-color: white;
      clip-path: ellipse(56% 100% at 50% -44%);
      position: absolute;
      z-index: 900;
   }
   img{
      width: 100%;
      object-fit: cover;
      transform: translate(0%, -26%);
   }
   .block-white-bottom{
      display: block;
      height: 100px;
      width: 100%;
      background-color: white;
      clip-path: ellipse(56% 100% at 50% 144%);
      position: absolute;
      bottom: 0;
   }
   .container{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

   }
}

</style>