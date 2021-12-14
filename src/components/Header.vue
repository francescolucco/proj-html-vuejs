<template>
  <header class="d-flex justify-content-between align-items-center">
    <div class="logo d-flex align-items-center">
      <img src="../assets/img/construction_logo_retina.png" alt="" />
    </div>
    <div class="menu-header d-flex justify-content-end align-items-center">
      <ul class="voice-menu d-flex justify-content-end align-items-center">
        <li
          v-for="(voice, index) in VoiceMenu"
          :key="index"
          @click="getActive(index)"
        >
          <a
            :class="{ active: voice.current }"
            class="d-flex justify-content-center align-items-center"
            href="#"
            >{{ voice.voicemenu }}
          </a>
        </li>
      </ul>
      <button class="yellow">GET QUOTE</button>
    </div>
  </header>
</template>

<script>
import VoiceMenu from "../assets/data/voice-menu";

export default {
  name: "Header",
  data() {
    return {
      VoiceMenu,
    };
  },

  methods: {
    getActive(index) {
      this.VoiceMenu.forEach((item) => {
        item.current = false;
      });
      this.VoiceMenu[index].current = true;
    },
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";

header {
  height: 125px;
  padding: 0 100px;
  .logo {
    height: 100%;
    img {
      height: 60%;
    }
  }
  .menu-header {
    height: 100%;
    .active {
      color: $second-color;
    }
  }
}
</style>
