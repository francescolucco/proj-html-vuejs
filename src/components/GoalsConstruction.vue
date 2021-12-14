<template>
  <div class="row">
    <div class="goals-construction col d-flex flex-column justify-content-center align-items-center" 
    v-for="(goal, index) in Goals" :key="index">
      <i 
      :class="goal.classe"
      class="fa-solid"></i>
      <h1>{{goal.number}}</h1>
      <h5 class="text-center">{{goal.text}}</h5>
    </div>
  </div>
</template>

<script>
import Goals from "../assets/data/goals-construction.js";
export default {
  name: "GoalsConstruction",
  data() {
    return {
      Goals,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";

.goals-construction{
   i{
      font-size: 90px;
      color: $second-color;
      padding-bottom: 5px;
   }
   h1{
      font-size: 70px;
      color: $second-color;
      padding-bottom: 5px;
   }
   h5{
      font-size: 20px;
      color: white;
   }
}

</style>
