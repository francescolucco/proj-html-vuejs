<template>
  <div class="row">
    <div v-for="(card, index) in Cards" :key="index" class="col">
      <div
        class="our-core-values front-card d-flex flex-column justify-content-center align-items-center"
        v-if="card.active"
      >
        <div
          class="box-icons d-flex justify-content-center align-items-center"
          :class="card.color"
        >
          <i :class="card.classe" class="fa-solid"> </i>
        </div>
        <div class="title">{{ card.title }}</div>
        <div class="line"></div>
        <p class="subtitle">{{ card.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import Cards from "../assets/data/our-core.js";
export default {
  name: "CardCoreValues",
  data() {
    return {
      Cards,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.row {
  padding: 0 100px;
  .our-core-values {
    padding: 25px 15px;
    &:hover {
      background-color: lighten($second-color, 35%);
      &:hover .box-icons {
        background-color: $second-color;
      }
      &:hover .title {
        color: $second-color;
      }
    }
    .box-icons {
      width: 110px;
      height: 110px;
      border-radius: 50%;
      &.azzurro {
        background-color: $azzurro;
      }
      &.blu {
        background-color: $blu;
      }
      &.arancione {
        background-color: $arancione;
      }
      &.verde {
        background-color: $verde;
      }
      i {
        font-size: 50px;
        color: white;
      }
    }
    .title {
      padding: 10px 0;
      font-size: 20px;
    }
    .line {
      display: block;
      height: 2px;
      background-color: lighten($titlecolor, 20%);
      width: 25px;
      margin-bottom: 20px;
    }
    .subtitle {
      text-align: center;
      font-size: 15px;
    }
  }
}
</style>
