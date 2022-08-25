<template>
  <div>
    <div class="row justify-content-center align-items-center">
      <div class="col-3">
        <ul>
          <li class="logo-size">
            <BaseLogo />
          </li>
          <li class="py-2">A Functional HTML Template for Corporate & Business.</li>
          <li>{{ phone }}</li>
          <li>{{ mail }}</li>
          <li>{{ street }}</li>
          <li class="mt-2"><BaseButton type="secondary" text="GET IN TOUCH" /></li>
        </ul>
      </div>
      <div class="col p-4">
        <ul>
          <li><h4 class="fw-bold">About</h4></li>
          <li v-for="(n, i) in about" :key="i">{{ n.link }}</li>
        </ul>
      </div>
      <div class="col mx-2 p-4">
        <ul>
          <li><h4 class="fw-bold">Transport</h4></li>
          <li v-for="(n, i) in transport" :key="i">{{ n.link }}</li>
        </ul>
      </div>
      <div class="col p-4">
        <ul>
          <li><h4 class="fw-bold">Support</h4></li>
          <li v-for="(n, i) in support" :key="i">{{ n.link }}</li>
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
  }
  ul{
    padding: 0;
  }

  .logo-size{
    width: 130px;
  }
</style>
