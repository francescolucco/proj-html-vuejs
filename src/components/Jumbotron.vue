<template>
<div>
  <div class="jumbotron d-flex justify-content-center align-items-center">
    <div class="text-jumbotron text-center">
      <h1 class="title-jumbotron">bilding unspring spaces</h1>
      <p>We Build Inspring Residential & Commercial Spaces</p>
      <div class="button-jumbotron">
        <button class="grey">EXPLORE RECENT WORK</button>
        <button class="yellow">GET A QUOTE TODAY</button>
      </div>
    </div>
  </div>
  <section class="d-flex justify-content-center align-items-center">
     <p>Do You Have A Construction Project We Can Help With?</p>
     <button class="grey">GET A FREE QUOTE</button>
  </section>
</div>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";

.jumbotron {
  background-image: url("../assets/img/home-slider-62528242.jpg");
  background-size: cover;
  background-position: center;
  height: 800px;
  margin: 0;
  .text-jumbotron{
     h1 {
       text-transform: uppercase;
       font-weight: 700;
       color: white;
       font-size: 55px;
     }
     p {
       color: $second-color;
       font-size: 23px;
       padding: 15px 0;
     }
     .button-jumbotron{
        button{
           margin: 10px;
        }
     }
  }
}
section{
   height: 160px;
   background-color: $second-color;
   color: $primary-color;
   position: relative;
   p{
      font-size: 30px;
   }
   button{
      position: absolute;
      top: 100%;
      left: 50%;
      transform: translate(-50%, -50%);
      border: 1px solid white;
   }
}
</style>
