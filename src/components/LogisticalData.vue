<template>
  <div>
    <div class="row justify-content-center text-center">
      <div class="col-4 py-5">
        <h5 class="logist pb-3 text-uppercase">How it Works in practice</h5>
        <h1><strong class="nome logist">Logistical</strong> Procedure</h1>
        <p class="py-3 text-secondary">
          We Work with innovative methodologies to ensure that the entire
          delivery process is done from start to finish as planned.
        </p>
      </div>
      <div class="time-line text-white d-flex justify-content-evenly mb-3 align-items-center">
        <div v-for="(n, i) in circle" :key="i" class="circle text-center">{{n.number}}</div>
      </div>
      <div class="row justify-content-center">
        <div class="col-2 px-3 mb-5" v-for="(logi, i) in logisticData" :key="i">
          <h5>{{ logi.procedureTitle }}</h5>
          <p>{{ logi.procedureDescription }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import data from "../data";

  export default {
    name: "LogisticalData",

    data() {
      return {
        ...data
      };
    },
  };
</script>
<style lang="scss">
  @import "src/assets/Images/sass/style.scss";

  .logist {
    color: $bluelagoon;
  }

  .time-line {
    height: 3px;
    background-color: rgba(123, 203, 206, 0.45)
  }

  .circle{
    border-radius: 50%;
    height: 30px;
    width: 30px;
    background-color: rgba(123, 203, 206, 0.9);
    color: $bluelagoon;
  }
</style>
