<template>
  <div class="jumbos-spaces">
    <div class="row">
      <div class="col-8 d-flex align-items-center">
        <div class="box-title d-flex justify-content-center flex-column">
          <p class="title">Building Inspiring Spaces</p>
          <div class="line"></div>
          <p class="subtitle">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas
            blanditiis consectetur sapiente. Accusantium nobis aliquid sed.
          </p>
        </div>
      </div>
      <div class="col-4 d-flex align-items-center justify-content-center flex-column">
         <button class="yellow">GET A FREE QUOTE</button>
         <p>Only takes a few seconds!</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "JumboSpaces",
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.jumbos-spaces {
  width: 100%;
  height: 500px;
  background-image: url("../assets/img/about-call-to-action-57862405.jpg");
  background-position: 50% 85%;
  .row {
    padding: 0 330px;
    height: 100%;
    .col-8 {
      height: 100%;
      .box-title {
         margin: 0;
        .title {
           padding-bottom: 30px;
           font-size: 45px;
           color: white;
        }
        .line {
          display: block;
          height: 2.5px;
          width: 250px;
          background-color: $second-color;
        }
        .subtitle {
          padding: 30px 0;
          width: 800px;
          text-align: start;
          color: white;
          font-size: 22px;
        }
      }
    }
    .col-4 {
      height: 100%;
      p{
        font-size: 15px;
        color: white;
        padding-top: 16px;
      }
    }
  }
}
</style>
