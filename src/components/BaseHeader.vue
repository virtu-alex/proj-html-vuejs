<template>
  <div>
    <div class="bg-dark text-white">
      <div
        class="container d-flex justify-content-between align-items-center py-2"
      >
        <div class="d-flex justify-content-evenly align-items-center w-25">
          <font-awesome-icon class="clock" icon="fa-solid fa-clock" />
          <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
        </div>
        <div class="d-flex justify-content-evenly align-items-center w-50">
          <div>
            <font-awesome-icon class="px-2" icon="fa-solid fa-phone" />
            <span>{{ phone }}</span>
          </div>
          <div>
            <font-awesome-icon class="px-2" icon="fa-solid fa-envelope" />
            <span>{{ mail }}</span>
          </div>
          <font-awesome-icon icon="fa-brands fa-facebook-f" />
          <font-awesome-icon icon="fa-brands fa-twitter" />
          <font-awesome-icon icon="fa-brands fa-linkedin-in" />
        </div>
      </div>
    </div>
    <div class="jumbotron">
      <div class="links container d-flex">
        <ul class="w-25 p-0">
          <li class="p-0">
            <BaseLogo />
          </li>
        </ul>
        <ul class="d-flex align-items-center justify-content-end w-75">
          <li><a href="">Home</a></li>
          <li class="px-4"><a href="#">About</a></li>
          <li class="px-4"><a href="#services">Services</a></li>
          <li class="px-4"><a href="#process">Process</a></li>
          <li class="px-4"><a href="#testimonials">Testimonial</a></li>
          <li>
            <font-awesome-icon class="user px-2" icon="fa-solid fa-user" />
          </li>
          <li><BaseButton text="get in touch" /></li>
        </ul>
      </div>
      <div class="container jumbotron-description">
        <div class="row">
          <div class="col-6">
            <h4 class="paragraph-title">Logistic Services</h4>
            <h1 class="subtitle text-white">Cargo Transport</h1>
            <p class="description">
              Fractional or exclusive road cargo transportation to all regions,
              with small, medium and large vehicles.
            </p>
            <div class="buttons-container">
              <BaseButton class="button-primary" text="get in touch" />
              <BaseButton type="secondary" text="read more" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import BaseButton from "./BaseButton.vue";
  import BaseLogo from "./BaseLogo.vue";

  import data from "../data";
  /* import the fontawesome core */
  import {library} from "@fortawesome/fontawesome-svg-core";

  /* import font awesome icon component */
  import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

  /* import specific icons */
  import {
    faPhone,
    faEnvelope,
    faUser,
    faClock,
  } from "@fortawesome/free-solid-svg-icons";
  import {
    faFacebookF,
    faTwitter,
    faLinkedinIn,
  } from "@fortawesome/free-brands-svg-icons";
  /* add icons to the library */
  library.add(
    faPhone,
    faEnvelope,
    faUser,
    faFacebookF,
    faTwitter,
    faLinkedinIn,
    faClock
  );

  export default {
    name: "BaseHeader",
    components: {BaseButton, FontAwesomeIcon, BaseLogo},
    data() {
      return {...data};
    },
  };
</script>

<style lang="scss">
  .jumbotron {
    background-image: url("/src/assets/Images/bg-9.jpg");
    background-size: cover;
    box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.6);
    & .logo {
      width: 150px;
    }
    & ul {
      list-style: none;
      & li {
        padding-left: 0.5rem;
        padding-right: 0.5rem;
        & a {
          text-decoration: none;
          text-transform: uppercase;
          color: white;
          font-weight: bold;
        }
      }
    }
  }
  .user {
    color: white;
  }
  .subtitle {
    font-size: 5rem;
    font-family: "Alfa Slab One", cursive;
    text-transform: uppercase;
  }
  .jumbotron-description {
    padding-top: 7rem;
    padding-bottom: 10rem;
    & .paragraph-title {
      color: #038384;
      text-transform: uppercase;
    }
  }
  .description {
    font-size: 1.5rem;
    color: grey;
  }

  .button-primary {
    margin-right: 20px;
  }
</style>
