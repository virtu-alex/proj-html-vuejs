<template>
  <div>
    <div class="border-bottom pt-2" v-for="(vehicle, i) in vehicleTypes" :key="i">
      <div class="row">
        <div class="col-4">
          <figure>
            <img
              class="truck-image"
              :src="require('@/assets/Images/truck-1.png')"
              alt=""
            />
          </figure>
        </div>
        <div class="col">
          <span class="vehicle-type"> {{ vehicle.type }}</span>
          <div class="weight">
            <span> {{ vehicle.weight }}</span>
          </div>
        </div>
      </div>
    </div>

    <div class="mt-4">
      <h5>Certifications</h5>
      <figure>
        <img
          v-for="n in 2"
          :key="n"
          class="certificate me-4"
          :src="require('../assets/Images/certificate.png')"
          alt=""
        />
      </figure>
    </div>
  </div>
</template>
<script>
  import data from "../data.js";
  export default {
    name: "VehicleType",
    components: {},
    data() {
      return {
        vehicleTypes: data["vehicleTypes"],
      };
    },
  };
</script>
<style lang="scss" scoped>
  .truck-image {
    width: 100%;
    background-color: #c5f1f3;
    padding: 5px;
  }

  .vehicle-type {
    font-weight: bold;
    font-size: 1.3rem;
  }
  .weight {
    color: grey;
  }

  .certificate {
    width: 110px;
    height: 110px;
  }

</style>
