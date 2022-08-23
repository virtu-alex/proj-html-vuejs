<template>
  <button :class="type === 'secondary' ? 'secondary' : ''" role="button">{{text}}</button>
</template>

<script>
  export default {
    name: "BaseButton",
    props: {
        text: String,
        type: String,
    }
  };
</script>

<style lang="scss" scoped>
  button {
    background-color: #038384;
    color: whitesmoke;
    border-radius: 5px;
    text-transform: uppercase;
    padding: 10px 20px;
    border: none;
  }
  .secondary{
      background-color: transparent;
      border: .5px solid #038384;
  }
</style>
