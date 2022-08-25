<template>
  <div class="row justify-content-center">
    <div
      class="col services me-3 p-4 mb-5"
      v-for="(service, i) in mainServices"
      :key="i"
    >
      <img
        class="icons position-relative"
        :src="require(`@/assets/Images/${service.pic}`)"
        alt="logo"
      />
      <!-- <img
        class="arrow position-absolute"
        :src="require(`@/assets/Images/${service.arrow}`)"
        alt="arrow"
      /> -->
      <h5 class="pt-3">{{ service.title }}</h5>
      <p class="py-3">{{ service.text }}</p>
    </div>
  </div>
</template>
<script>
  import data from "../data";

  export default {
    name: "ServiceCard",
    data() {
      return {
        mainServices: data["mainServices"],
      };
    }
  };
</script>
<style lang="scss" scoped>
  @import "src/assets/Images/sass/style.scss";

  .services {
    background-color: $shark;
    border-radius: 10px;
  }

  .icons {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    padding: 5px;
    background-color: rgb(123, 203, 206, 0.3);
    color: #038384;
  }
</style>
