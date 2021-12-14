<template>
  <div class="container">
    <div class="d-flex justify-content-center align-items-center">
      <div
        v-for="(card, index) in Cards"
        :key="index"
        class="box-recent-work"
        @mouseover="mouseOver(index)"
        @mouseout="mouseOut(index)"
      >
        <div class="box-img" v-if="card.active">
          <img :src="require(`../assets/img/${card.img}`)" alt="" />
        </div>

        <div
          class="d-flex flex-column justify-content-center align-items-center text-recent-work"
          v-else
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
          <p class="subtitle-recent">{{ card.type }}</p>
        </div>
      </div>
    </div>
    <div class="all-projects d-flex justify-content-center align-items-center">
      <div class="line"></div>
      <p>view all projects</p>
      <div class="line"></div>
    </div>
  </div>
</template>

<script>
import Cards from "../assets/data/recent-work.js";
export default {
  name: "ResentWork",
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

.box-recent-work {
  height: 400px;
  width: 400px;
  background-color: $second-color;
  margin: 20px 20px 70px 20px;
  padding: 0;
  .box-img {
    width: 100%;
    height: 100%;
    img {
      width: 100%;
      height: 100%;
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
