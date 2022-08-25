<template>
  <div id="app">
    <header><BaseHeader /></header>
    <main>
      <BaseMain />
    </main>
    <footer>
      <BaseFooter />
      <section class="below-footer text-white">
        <div class="container">
          <div class="row justify-content-between py-2">
            <div class="col-6">
              Enjoy the low price. We are tracking any intention of piracy.
            </div>
            <div class="col-6 text-end">
              &copy; 2020 NEXGEN is Proudly Powered by
              <strong class="presentation">Codings</strong>
            </div>
          </div>
        </div>
      </section>
    </footer>
  </div>
</template>

<script>
  import BaseHeader from "./components/BaseHeader.vue";
  import BaseMain from "./components/BaseMain.vue";
  import BaseFooter from "./components/BaseFooter.vue";

  export default {
    name: "App",
    components: {BaseHeader, BaseMain, BaseFooter},
  };
</script>

<style lang="scss">
  @import "src/assets/Images/sass/style.scss";
</style>
