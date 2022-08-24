<template>
  <div>
    <img
      class="logo img-fluid pt-2"
      :src="require('@/assets/Images/logo.svg')"
      alt="logo"
    />
  </div>
</template>
<script>
  export default {
    name: "BaseLogo",
  };
</script>
<style lang="scss">
  .logo {
    width: 150px;
  }
</style>
