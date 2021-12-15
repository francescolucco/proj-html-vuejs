<template>
  <div class="container">
    <div class="d-flex justify-content-center align-items-center">
      <div
        v-for="(card, index) in Cards"
        :key="index"
        class="box-latst-news"
        @mouseover="mouseOver(index)"
        @mouseout="mouseOut(index)"
      >
        <div class="front-card">
          <div class="box-cont">
            <img
              :src="require(`../assets/img/${card.image}`)"
              alt=""
              v-if="card.active"
            />
            <div
              v-else
              class="d-flex flex-column justify-content-center align-items-center text-recent-work"
            >
              <div
                class="box-icons d-flex justify-content-center align-items-center"
              >
                <div
                  class="box-font d-flex justify-content-center align-items-center"
                >
                  <i class="fa-solid fa-link"></i>
                </div>
                <div
                  class="box-font d-flex justify-content-center align-items-center"
                >
                  <i class="fa-light fa-magnifying-glass-plus"></i>
                </div>
              </div>
              <div class="title-recent">{{ card.title }}</div>
              <p class="subtitle-recent">{{ card.place }}</p>
            </div>
          </div>
          <div class="box-text-latest-news">
            <div class="title-latest-news">{{ card.title }}</div>
            <div class="date-latest-news">{{ card.date }}</div>
            <div class="line-latest-news"></div>
            <div class="date-latest-news">{{ card.text }}</div>
          </div>
        </div>
      </div>
    </div>
    <div class="all-projects d-flex justify-content-center align-items-center">
      <div class="line"></div>
      <p>view all articles</p>
      <div class="line"></div>
    </div>
  </div>
</template>

<script>
import Cards from "../assets/data/latest-news.js";
export default {
  name: "LatestNews",
  data() {
    return {
      Cards,
    };
  },
  methods: {
    mouseOver(index) {
      this.Cards[index].active = false;
    },
    mouseOut(index) {
      this.Cards[index].active = true;
    },
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.box-latst-news {
  height: auto;
  width: 400px;
  background-color: $second-color;
  margin: 20px 20px 70px 20px;
  padding: 0;
  .front-card {
    width: 100%;
    height: 100%;
    background-color: white;
    .box-cont {
      width: 100%;
      height: 60,25%;
      background-color: $second-color;
    }
    img {
      width: 100%;
    }
    .box-text-latest-news {
      padding: 25px;
      .title-latest-news {
        font-size: 24px;
        padding-bottom: 6px;
      }
      .date-latest-news {
        font-size: 12px;
        padding-bottom: 18px;
      }
      .line-latest-news {
        display: block;
        width: 100%;
        height: 2px;
        background-color: lighten($primary-color, 50%);
        margin-bottom: 28px;
      }
      .date-latest-news {
        font-size: 15px;
        line-height: 30px;
        padding-bottom: 18px;
      }
    }
  }
  .text-recent-work {
    width: 100%;
    height: 100%;
    padding: 30px;
    text-align: center;
    .box-font {
      width: 40px;
      height: 40px;
      background-color: white;
      margin: 15px 5px;
      border-radius: 50%;
      i {
        color: $second-color;
        font-size: 16px;
      }
    }
    .title-recent {
      color: white;
      font-size: 18px;
    }
    .subtitle-recent {
      color: white;
      font-size: 13px;
    }
  }
}
.all-projects {
  .line {
    width: 400px;
    height: 2px;
    background-color: lighten($titlecolor, 50%);
    display: block;
    margin: 20px 20px 50px 20px;
  }
  p {
    width: 400px;
    text-transform: uppercase;
    font-size: 15px;
    text-align: center;
    padding-top: 10px;
    margin: 20px 20px 50px 20px;
  }
}
</style>
