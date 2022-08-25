<template>
  <button :class="type === 'secondary' ? 'secondary' : ''" role="button">
    {{ text }}
  </button>
</template>

<script>
  export default {
    name: "BaseButton",
    props: {
      text: String,
      type: String,
    },
  };
</script>

<style lang="scss" scoped>
  @import "src/assets/Images/sass/style.scss";

  button {
    background-color: $bluelagoon;
    color: whitesmoke;
    border-radius: 5px;
    text-transform: uppercase;
    padding: 10px 20px;
    border: none;
  }
  
  button:hover {
    filter: brightness(105%);
    border: inset 1px white;
  }
  .secondary {
    background-color: transparent;
    border: 1px solid $bluelagoon;
    padding-left: 20px;
    padding-right: 20px;
  }

</style>
