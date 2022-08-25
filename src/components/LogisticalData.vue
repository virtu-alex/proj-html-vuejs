<template>
  <div>
    <div v-for="(logi, i) in logisticData" :key="i" class="row justify-content-center">
        <div class="col-8 text-center">
          <h5>How it Works in practice</h5>
          <h1>Logistical Procedure</h1>
          <p>
            {{logi.subtitle}}
          </p>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-2">
          <h5>Collection of information</h5>
          <p>{{ halfLorem }}</p>
        </div>
  </div>
</template>
<script>
  import data from "../data";

  export default {
    name: "LogisticalData",

    data() {
      return {
        logisticData: data["logisticData"],
      };
    },
  };
</script>
<style lang=""></style>
