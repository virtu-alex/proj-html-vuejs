<template>
  <div>
    <div class="contact-bar">
      <div>
        <font-awesome-icon class="clock" icon="fa-solid fa-clock" />
        <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
      </div>
      <div>
        <BaseContacts />
        
      </div>
    </div>
    <BaseButton text="get in touch" />
    <BaseButton type="secondary" text="read more" />
  </div>
</template>

<script>
  import BaseButton from "./BaseButton.vue";
  import BaseContacts from "./BaseContacts.vue";
  /* import the fontawesome core */
  import {library} from "@fortawesome/fontawesome-svg-core";

  /* import font awesome icon component */
  import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

  /* import specific icons */
  import {faClock} from "@fortawesome/free-solid-svg-icons";

  /* add icons to the library */
  library.add(faClock);

  export default {
    name: "BaseHeader",
    components: {BaseButton, FontAwesomeIcon, BaseContacts},
    data() {
      return {};
    },
  };
</script>

<style lang="scss" scoped>
  .contact-bar {
    background-color: #191c1e;
    height: 30px;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: white;
  }

  .clock {
    padding-right: 8px;
  }
</style>
