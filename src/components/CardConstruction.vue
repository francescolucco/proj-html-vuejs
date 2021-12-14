<template>
  <div class="row">
    <div v-for="(card, index) in Cards" :key="index" class="col"
     @mouseover="mouseOver(index)"
     @mouseout="mouseOut(index)">
      <div
        class="card-construction front-card d-flex flex-column justify-content-center align-items-center"
        v-if="card.active"
      >
        <div class="box-icons d-flex justify-content-center align-items-center">
          <i :class="card.classe" class="fa-solid"> </i>
        </div>
        <div class="title">{{ card.title }}</div>
        <p class="subtitle">{{ card.text }}</p>
      </div>

      <div
        class="card-construction retro-card d-flex flex-column justify-content-center align-items-center"
        v-else
      >
        <div class="title">{{ card.title }}</div>
        <p class="subtitle">{{ card.text }}</p>
        <button class="yellow custom">GET A QUOTE</button>
      </div>
    </div>
  </div>
</template>

<script>
import Cards from "../assets/data/card-construction.js";
export default {
  name: "CardConstruction",
  data() {
    return {
      Cards,
    };
  },
  methods: {
    mouseOver(index) {
      this.Cards[index].active = false
    },
    mouseOut(index) {
      this.Cards[index].active = true
    },
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/utilities.scss";

.card-construction {
  background-color: #f5f5f5;
  border-radius: 10px;
  padding: 25px;
  height: 372px;
  .box-icons {
    width: 60px;
    height: 60px;
    border: 1px solid $primary-color;
    border-radius: 50%;
    i {
      font-size: 25px;
    }
  }
  .title {
    padding: 10px 0;
  }
  .subtitle {
    text-align: center;
  }
}
.retro-card {
  background-color: $second-color;
  .title {
    text-transform: uppercase;
  }
  button.yellow.custom {
    background-color: lighten($second-color, 15%);
    &:hover {
      background-color: #f5f5f5;
      color: $primary-color;
    }
  }
}
</style>
