<template>
  <div class="row justify-content-center">
    <div
      class="col services me-3 p-4 mb-5"
      v-for="(service, i) in mainServices"
      :key="i"
    >
      <img
        class="icons"
        :src="require(`@/assets/Images/${service.pic}`)"
        alt=""
      />
      <img
        class="arrow"
        :src="require(`@/assets/Images/${service.arrow}`)"
        alt=""
      />
      <h5>{{ service.title }}</h5>
      <p>{{ service.text }}</p>
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
    },
    components: {},
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

  .arrow {
    width: 30px;
    top: 10px;
    right: 0;
  }
</style>
