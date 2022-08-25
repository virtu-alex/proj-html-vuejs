<template>
  <div>
    <div class="row">
      <div class="col-3 text-secondary">
        <ul>
          <li class="logo-size">
            <BaseLogo />
          </li>
          <li class="py-2">
            A Functional HTML Template <br />
            for Corporate & Business.
          </li>
          <li>{{ phone }}</li>
          <li>{{ mail }}</li>
          <li>{{ street }}</li>
          <li class="mt-2">
            <BaseButton type="secondary" text="GET IN TOUCH" />
          </li>
        </ul>
      </div>
      <div class="col text-center p-4">
        <ul>
          <li><h4 class="fw-bold text-white">About</h4></li>
          <li v-for="(about, i) in abouts" :key="i"><a href="">{{ about.link }}</a></li>
        </ul>
      </div>
      <div class="col text-center mx-2 p-4">
        <ul>
          <li><h4 class="fw-bold text-white">Transport</h4></li>
          <li v-for="(transport, i) in transports" :key="i"><a href="">{{ transport.link }}</a></li>
        </ul>
      </div>
      <div class="col text-center p-4">
        <ul>
          <li><h4 class="fw-bold text-white">Support</h4></li>
          <li v-for="(support, i) in supports" :key="i"><a href="">{{ support.link }}</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
  import data from "../data";
  import BaseButton from "./BaseButton.vue";
  import BaseLogo from "./BaseLogo.vue";

  export default {
    name: "FooterList",
    data() {
      return {
        ...data,
      };
    },
    components: {
      BaseButton,
      BaseLogo,
    },
  };
</script>
<style lang="scss" scoped>
  @import "src/assets/Images/sass/style.scss";

  .col {
    background-color: rgba($midgray, $alpha: 0.1);
    border-radius: 5px;
    font-size: 1.15rem;
    color: $silversand;
  }
  ul {
    padding: 0;
  }

  .logo-size {
    width: 130px;
  }

  a{
    text-decoration: none;
    color: $silversand;
  }
</style>
