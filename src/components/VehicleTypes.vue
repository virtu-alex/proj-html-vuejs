<template>
  <div>
    <img :src="require('@/assets/Images/truck-1.png')" alt="" />
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum, id amet nihil exercitationem quas eum ut in eaque magnam, consequuntur dignissimos sapiente quam ullam accusamus ipsa, recusandae tenetur consequatur sequi!</p>
  </div>
</template>
<script>
  export default {
    name: "VehicleTypes",
    props: {text: String, type: String},
    data() {
        return {

        }
    },
  };
</script>
<style lang="scss" scoped></style>
