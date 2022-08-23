<template>
  <div>
    <font-awesome-icon icon="fa-solid fa-phone" />
    <span>{{ phone }}</span>
    <font-awesome-icon icon="fa-solid fa-envelope" />
    <span>{{ mail }}</span>
    <font-awesome-icon icon="fa-brands fa-facebook-f" />
    <font-awesome-icon icon="fa-brands fa-twitter" />
    <font-awesome-icon icon="fa-brands fa-linkedin-in" />
  </div>
</template>
<script>
  import {library} from "@fortawesome/fontawesome-svg-core";

  /* import font awesome icon component */
  import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

  /* import specific icons */
  import {
    faPhone,
    faEnvelope,
  } from "@fortawesome/free-solid-svg-icons";
  import {
    faFacebookF,
    faTwitter,
    faLinkedinIn,
  } from "@fortawesome/free-brands-svg-icons";

  /* add icons to the library */
  library.add(faPhone, faEnvelope);
  library.add( faFacebookF, faTwitter, faLinkedinIn);
//   faFacebook, faTwitter, faLinkedin
  export default {
    name: "BaseContacts",
    components: {FontAwesomeIcon},
    data() {
      return {
        phone: "+1 (305) 1234-5678",
        mail: "hello@example.com",
      };
    },
  };
</script>
<style lang="scss" scoped></style>
