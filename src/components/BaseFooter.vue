<template>
  <section class="footer bg-dark py-5 text-white">
    <footer>
      <div class="container">
        <FooterList />
      </div>
    </footer>
  </section>
</template>
<script>
  import FooterList from "./FooterList.vue";
  export default {
    name: "BaseFooter",
    components: {
      FooterList,
    },
  };
</script>
<style lang="scss" scoped>
  .below-footer {
    height: 40px;
    background-color: rgb(8, 8, 8);
  }
</style>
