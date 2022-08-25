<template>
  <div id="app">
    <header><BaseHeader /></header>
    <main>
      <BaseMain />
    </main>
    <footer></footer>
  </div>
</template>

<script>
  import BaseHeader from "./components/BaseHeader.vue";
  import BaseMain from "./components/BaseMain.vue";

  export default {
    name: "App",
    components: {BaseHeader, BaseMain},
  };
</script>

<style lang="scss">
  @import "src/assets/Images/sass/style.scss";

  
</style>
