<template>
  <footer>
    <div class="row">
      <div class="col-3 one">
        <img src="../assets/img/footer-logo.png" alt="" />
        <p>
          We are specialist in the construction of unique and exclusive
          proprierties. our work inspires. We pride ourselves on delivering
          outstanding quality and design for leading clients across the world.
        </p>
        <button class="yellow">LEARN MORE</button>
      </div>
      <div class="col-3 two">
        <div class="title-footer">latest tweets</div>
        <div class="row">
          <div class="col-2">
            <img
              src="../assets/img/3a74ce3d0532b7773b174c45ca3bd05a_normal.png"
              alt=""
            />
          </div>
          <div class="col-10">
            <img class="tweet" src="../assets/img/image (1).svg" alt="" />
            <div class="strong">ThemeFusion</div>
            <div class="twetter">@Theme_Fusion</div>
            <div class="text">
              Do you need sublime WordPress hosting for your next website? take
              advantage of exclusive partner offers that we have secured just
              for you, & launch your site in seconds width
              <span>#avada</span> on WP Engine hosting & get 30% Off this Black
              Friday <span>bit.ly/3kjLLE2 #BlackFriday2020</span>
            </div>
            <img src="../assets/img/En2TRxLW4AEiWUN.jpeg" alt="" />
            <div class="box-icons-footer d-flex justify-content-start">
              <img src="../assets/img/image (2).svg" alt="" />
              <img src="../assets/img/image (3).svg" alt="" />
            </div>
          </div>
        </div>
      </div>
      <div class="col-3 three"></div>
      <div class="col-3 four"></div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/mixin.scss";
@import "../assets/styles/generals.scss";
@import "../assets/styles/utilities.scss";

footer {
  width: 100%;
  height: 850px;
  background-color: #1e1e1e;
  margin: 0;
  padding: 65px 80px;
  .col-3 {
    padding: 10px;
    height: 100%;
  }
  .one {
    img {
      padding-bottom: 45px;
    }
    p {
      padding-bottom: 20px;
    }
  }
  .two {
    .title-footer {
      color: $second-color;
      font-size: 18px;
      text-transform: uppercase;
      font-weight: 500;
      padding-bottom: 40px;
      position: relative;
    }
    .row {
      padding: 0;
      margin: 0;
      .col-2 {
        padding: 0;
        margin: 0;
      }
      .col-10 {
        padding: 0;
        margin: 0;
        .tweet {
          position: absolute;
          width: 22px;
          top: 0;
          right: 0;
          cursor: pointer;
        }
        .strong {
          color: white;
          font-weight: 700;
        }
        .twetter {
          color: white;
          font-size: 15px;
        }
        .text {
          color: white;
          span {
            color: #27628f;
          }
        }
        img {
          width: 100%;
        }
        .box-icons-footer {
          img {
            width: 20px;
            margin-right: 20px;
            cursor: pointer;
          }
        }
      }
    }
  }
  .three {
  }
  .four {
  }
}
</style>
