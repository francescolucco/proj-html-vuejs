<template>
  <footer>
    <div class="footer-top">
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
                Do you need sublime WordPress hosting for your next website?
                take advantage of exclusive partner offers that we have secured
                just for you, & launch your site in seconds width
                <span>#avada</span> on WP Engine hosting & get 30% Off this
                Black Friday <span>bit.ly/3kjLLE2 #BlackFriday2020</span>
              </div>
              <img src="../assets/img/En2TRxLW4AEiWUN.jpeg" alt="" />
              <div class="box-icons-footer d-flex justify-content-start">
                <img src="../assets/img/image (2).svg" alt="" />
                <img src="../assets/img/image (3).svg" alt="" />
              </div>
            </div>
          </div>
        </div>
        <div class="col-3 three">
          <div class="title-footer">contact us today</div>
          <ul class="ul-footer">
            <li
              v-for="(info, index) in Informations"
              :key="index"
              class="li-footer d-flex"
            >
              <div class="box-icon">
                <i class="fa-solid" :class="info.classe"></i>
              </div>
              <div class="box-text">
                <p>{{ info.text }}</p>
              </div>
            </li>
          </ul>
        </div>
        <div class="col-3 four">
          <div class="title-footer">contact us today</div>
          <img src="../assets/img/construction_map_pin.png" alt="" />
        </div>
      </div>
    </div>
    <div class="footer-bottom d-flex justify-content-lg-between align-items-center">
       <div class="box-text-f-bottom">
          COPIRIGHT 2012 . 2015 AVADA THEME BY THEME FUSION | POWERED BY WORDPRESS
       </div>
       <div class="box-icons-f-bottom d-flex justify-content-end align-items-center">
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-youtube"></i>
          <i class="fa-brands fa-instagram"></i>

       </div>
    </div>
  </footer>
</template>

<script>
import Informations from "../assets/data/ul-footer";
export default {
  name: "Footer",
  data() {
    return {
      Informations,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/mixin.scss";
@import "../assets/styles/generals.scss";
@import "../assets/styles/utilities.scss";

.footer-top {
  width: 100%;
  background-color: #1e1e1e;
  margin: 0;
  padding: 65px 80px 0 80px;
  .row {
    padding: 0 0 80px 0;
    .col-3 {
      padding: 10px;
      height: 100%;
    }
    .one {
      padding: 0 30px 0 0;
      img {
        padding-bottom: 45px;
      }
      p {
        padding-bottom: 17px;
        &:hover {
          color: white;
        }
      }
      button {
        &:hover {
          border: 1px solid white;
        }
        &:hover p {
          color: white;
        }
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
          padding: 0 30px 0 0;
          .tweet {
            position: absolute;
            width: 22px;
            top: -25px;
            right: 30px;
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
            margin-top: 25px;
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
      .title-footer {
        color: $second-color;
        font-size: 18px;
        text-transform: uppercase;
        font-weight: 500;
        padding-bottom: 40px;
        position: relative;
      }
      .ul-footer {
        padding: 0;
        margin: 0;
        .li-footer {
          padding: 3px 0;
          margin: 0;
          text-transform: none;
          &:hover .box-icon i {
            color: white;
            cursor: pointer;
          }
          &:hover .box-text p {
            color: white;
            cursor: pointer;
          }
          .box-icon {
            height: 100%;
            width: 8%;
            i {
              font-size: 22px;
              padding-top: 7px;
            }
          }
          .box-text {
            width: 75%;
            p {
              font-size: 17px;
            }
          }
        }
      }
    }
    .four {
      .title-footer {
        color: $second-color;
        font-size: 18px;
        text-transform: uppercase;
        font-weight: 500;
        padding-bottom: 40px;
        position: relative;
      }
      img {
        width: 100%;
      }
    }
  }
}
.footer-bottom {
  height: 85px;
  background-color: black;
  width: 100%;
  padding: 0 80px;
  .box-text-f-bottom{
     font-size: 13px;
  }
  .box-icons-f-bottom{
     i{
        margin:0 0 0 22px;
        font-size: 18px;
        cursor: pointer;
        &:hover{
           color: white;
        }
     }
  }
}
</style>
