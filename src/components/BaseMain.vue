<template>
  <section class="who-we-are">
    <div class="container">
      <div class="row">
        <div class="col-8 title">
          <h5>WHO WE ARE</h5>
          <h1>Excellence in Transport</h1>
          <p class="py-2 text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non quam,
            sit nam vel quaerat ad facilis et praesentium adipisci odit
            temporibus distinctio sunt quod natus veritatis tempore fugit
            similique animi.
          </p>
          <p class="py-3 text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non quam,
            sit nam vel quaerat ad facilis et praesentium adipisci odit
            temporibus distinctio sunt quod natus veritatis tempore fugit
            similique animi.
          </p>
          <p class="py-3 comment">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non quam,
            sit nam vel quaerat ad facilis et praesentium adipisci odit
            temporibus distinctio sunt quod natus veritatis tempore fugit
            similique animi.
          </p>
          <p class="py-3 text-secondary">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non quam,
            sit nam vel quaerat ad facilis
          </p>
          <ul class="text-secondary">
            <li>Lorem ipsum dolor sit amet</li>
            <li>consectetur adipisicing elit</li>
            <li>Non quam, sit nam vel</li>
            <li>dolor sit amet consectetur adipisicing elit</li>
            <li>sunt quod natus veritatis tempore fugit</li>
          </ul>
        </div>
        <div class="col-4">
          <h5>Vehicle Types</h5>
          <VehicleTypes />
        </div>
      </div>
    </div>
  </section>
</template>


<script>


  import VehicleTypes from "./VehicleTypes.vue";

  export default {
    name: "BaseMain",
    componets: {
      VehicleTypes,
    },
  };
</script>
<style lang="scss">
  .who-we-are {
    padding-top: 100px;
  }

  .comment {
    border-left: 4px solid rgb(96, 157, 159, 0.4);
    padding-left: 20px;
    font-style: italic;
    color: grey;
  }
</style>
