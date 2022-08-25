<template>
  <div class="container pt-5">
    <div class="row justify-content-center">
      <div class="col-8 text-center pb-3">
        <h5 class="presentation">Customer testimonials</h5>
        <h1 class="py-2">Trusted <strong class="nome">Feedback</strong></h1>
        <p>
          We Work intensively in search of ideals that can add up in the lives
          of our curstomers. This is what moves us and we are grateful for the
          recognition.
        </p>
      </div>
    </div>
    <div class="row justify-content-center">
      <div
        v-for="(feedback, i) in feedbacksData"
        :key="i"
        class="col p-3 me-3 feedback-card"
      >
        <img
          class="filter my-3"
          :src="require(`@/assets/Images/${feedback.pic}`)"
          alt="WooCommerce"
        />
        <p>{{ feedback.text }}</p>
      </div>
    </div>
  </div>
</template>
<script>
  import data from "../data";

  export default {
    name: "CustomersFeedbacks",

    data() {
      return {
        feedbacksData: data["feedbacksData"],
      };
    },
  };
</script>
<style lang="scss" scoped>
  .filter {
    filter: brightness(1000%);
    width: 120px;
  }
</style>
