<template>
  <div class="row justify-content-center">
    <div class="col services me-2 p-4" v-for="(service, i) in mainServices" :key="i">
      <!-- <img :src="require('{{service.pic}}')" alt="" /> -->
      <h5>{{ service.title }}</h5>
      <p>{{ service.text }}</p>
      <!-- <font-awesome-icon class="px-2" :icon="`{{service.pic}}`" /> -->
    </div>
  </div>
</template>
<script>
  import data from "../data";

  import {library} from "@fortawesome/fontawesome-svg-core";

  /* import font awesome icon component */
  // import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

  /* import specific icons */
  import {
    faTruck,
    faTemperatureLow,
    faLaptop,
  } from "@fortawesome/free-solid-svg-icons";

  library.add(faTruck, faTemperatureLow, faLaptop);
  export default {
    name: "ServiceCard",
    data() {
      return {
        mainServices: data["mainServices"],
      };
    },
    components: {
      // FontAwesomeIcon,
    },
  };
</script>
<style lang="scss">
  .services {
    background-color: #191c1e;
  }
</style>
