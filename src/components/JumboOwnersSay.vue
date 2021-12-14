<template>
  <div class="section-img-curve">
    <div class="block-white-top-a"></div>
    <img src="../assets/img/home-parallax-144609983.jpg" alt="" />
    <div class="block-white-bottom-a"></div>
    <div class="container d-flex justify-content-center align-items-center">
      <div
        class="box-title-fl d-flex justify-content-center align-items-center flex-column"
      >
        <p class="title">Our Home Owners Say</p>
        <div class="line"></div>
        <img src="../assets/img/home-testimonial-113165296.jpg" alt="" />
        <p class="subtitle">
          "no man but feels more of a man in the world if he have but a bit of
          ground that he can call his own. However small it is on the surface,
          it is four thousand miles deep: and that is a very handsome property."
        </p>
        <div
          class="box-author d-flex justify-content-center align-items-center"
        >
          <p>HARRY SMITH</p>
          <div class="point"></div>
          <p>NEW HOME OWNER</p>
        </div>
        <div class="box-point d-flex justify-content-center align-items-center">
          <div class="point"></div>
          <div class="point empty"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "JumboOwnersSay",
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";
.section-img-curve {
  margin: 100px 0;
  height: 700px;
  overflow: hidden;
  position: relative;
  .block-white-top-a {
    display: block;
    height: 100px;
    width: 100%;
    background-color: #f5f5f5;
    clip-path: ellipse(56% 100% at 50% -44%);
    position: absolute;
    z-index: 900;
  }
  img {
    width: 100%;
    object-fit: cover;
    transform: translate(0%, -26%);
  }
  .block-white-bottom-a {
    display: block;
    height: 100px;
    width: 100%;
    background-color: #f5f5f5;
    clip-path: ellipse(56% 100% at 50% 144%);
    position: absolute;
    bottom: 0;
  }
  .container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .box-title-fl {
    .title {
      padding: 5px 0;
      color: white;
    }
    .line {
      display: block;
      height: 2px;
      width: 200px;
      background-color: $second-color;
      margin-bottom: 50px;
    }
    img {
      width: 110px;
      height: 110px;
      border-radius: 50%;
    }
    .subtitle {
      width: 660px;
      text-align: center;
      font-weight: 400;
      font-style: italic;
      color: white;
      font-size: 18px;
    }
    .box-author {
      p {
        color: white;
        font-weight: 600;
        font-size: 18px;
        margin: 0;
      }
      .point {
        margin: 0px 10px;
        display: block;
        height: 4px;
        width: 4px;
        border-radius: 50%;
        background-color: white;
      }
    }
    .box-point {
      height: 15px;
      width: 100px;
      margin-top: 40px;
      .point {
        margin: 0px 5px;
        display: block;
        height: 10px;
        width: 10px;
        border-radius: 50%;
        background-color: white;
      }
      .point.empty {
        background-color: transparent;
        border: 1px solid white;
      }
    }
  }
}
</style>
