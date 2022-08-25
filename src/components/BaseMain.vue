<template>
  <div>
    <!-- WHO WE ARE SECTION -->
    <section class="who-we-are">
      <div class="container">
        <div class="row">
          <div class="col-8 title text-secondary">
            <h5 class="presentation pb-2">WHO WE ARE</h5>
            <h1>
              <strong class="nome p-1">
                <font-awesome-icon icon="fa-solid fa-gem" /><strong
                  class="p-0 color-swap"
                >
                  Excellence</strong
                > </strong
              ><strong class="px-2 text-black">in Transport</strong>
            </h1>
            <p class="py-2">
              {{ lorem }}
            </p>
            <p class="py-3">
              {{ lorem }}
            </p>
            <p class="py-3 comment">
              {{ lorem }}
            </p>
            <p class="py-3">
              {{ halfLorem }}
            </p>
            <ul class="">
              <li v-for="(description, i) in transportDescription" :key="i">
                {{ description.text }}
              </li>
            </ul>
          </div>
          <div class="col-4">
            <h5>Vehicle Types</h5>
            <VehicleTypes />
          </div>
        </div>
      </div>
    </section>
    <!-- MAIN SERVICES SECTION -->
    <section id="services" class="main-services pt-5 text-white bg-dark">
      <div class="container">
        <div class="row">
          <div class="col-7 p-0">
            <h5 class="presentation pb-3">ROAD TRANSPORT</h5>
          </div>
          <h2 class="px-0 pb-3">
            <strong>Main</strong> <strong class="nome">Services</strong>
          </h2>
          <div class="row p-0">
            <div class="col-7">
              <p class="py-3">
                {{ expertiseText }}
              </p>
            </div>
            <div class="col-5 text-end py-3">
              <BaseButton text="See All" type="secondary" />
            </div>
          </div>
        </div>
        <ServiceCard />
      </div>
    </section>
    <!-- LOGISTICAL SECTION -->
    <section id="process" class="logistical pt-5">
      <LogisticalData />
    </section>
    <!-- RESULTS SECTION -->
    <section id="testimonials" class="results text-white">
      <div class="container">
        <div class="row justify-content-center text-center">
          <div class="col-6 py-3">
            <h5 class="pb-3 presentation">What are we doing</h5>
            <h1><strong class="nome">Results</strong> in Numbers</h1>
          </div>
          <div class="row py-5 mt-3 text-center fw-bold">
            <div class="col-3 presentation">
              <h3>128</h3>
              <p class="text-white">Certifications</p>
            </div>
            <div class="col-3 presentation">
              <h3>230</h3>
              <p class="text-white">Employees</p>
            </div>
            <div class="col-3 presentation">
              <h3>517</h3>
              <p class="text-white">Customers</p>
            </div>
            <div class="col-3 presentation">
              <h3>94</h3>
              <p class="text-white">Countries Served</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- TRUSTED FEEDBACK SECTION -->
    <section class="feedback bg-dark text-white">
      <CustomersFeedback />
    </section>
    <!-- SEND A MESSAGE SECTION -->
    <section class="send-message">
      <div class="container pt-5">
        <div class="row align-items-center">
          <BaseForm />
          <div class="col-5">
            <ul>
              <li><h4>Example Inc.</h4></li>
              <li class="py-2">
                <p>{{ halfLorem }}</p>
              </li>
              <li class="py-1">
                <p>{{ halfLorem }}</p>
              </li>
              <li class="py-3 d-flex align-items-center">
                <font-awesome-icon
                  class="contacts-icons"
                  icon="fa-solid fa-phone"
                />
                <span class="px-2 color-swap">{{ phone }}</span>
              </li>
              <li class="py-3 d-flex align-items-center">
                <font-awesome-icon
                  class="contacts-icons"
                  icon="fa-solid fa-envelope"
                />
                <span class="px-2 color-swap">{{ mail }}</span>
              </li>
              <li class="py-3 d-flex align-items-center">
                <font-awesome-icon
                  class="contacts-icons"
                  icon="fa-solid fa-compass"
                />
                <span class="px-2 color-swap">{{ street }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
   
  </div>
</template>

<script>
  import BaseButton from "./BaseButton.vue";
  import CustomersFeedback from "./CustomersFeedback.vue";
  import LogisticalData from "./LogisticalData.vue";
  import BaseForm from "./BaseForm.vue";
  import ServiceCard from "./ServiceCard.vue";
  import data from "../data";
  import VehicleTypes from "./VehicleTypes.vue";
  import {library} from "@fortawesome/fontawesome-svg-core";

  /* import font awesome icon component */
  import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

  /* import specific icons */
  import {
    faPhone,
    faEnvelope,
    faCompass,
    faGem,
  } from "@fortawesome/free-solid-svg-icons";

  /* add icons to the library */
  library.add(faPhone, faEnvelope, faCompass, faGem);
  export default {
    name: "BaseMain",
    components: {
      VehicleTypes,
      BaseButton,
      FontAwesomeIcon,
      BaseForm,
      ServiceCard,
      LogisticalData,
      CustomersFeedback,
    },
    data() {
      return {...data};
    },
  };
</script>
<style lang="scss">
  @import "src/assets/Images/sass/style.scss";

  .who-we-are {
    padding-top: 100px;
    padding-bottom: 100px;
  }

  .presentation {
    color: $bluelagoon;
    font-size: 0.9rem;
    text-transform: uppercase;
    font-weight: bold;
  }

  .comment {
    border-left: 5px solid rgb($bluelagoon, 0.2);
    padding-left: 20px;
    font-style: italic;
  }

  .color-swap {
    color: $bluelagoon;
  }

  .results {
    background-image: url("/src/assets/Images/bg-10.jpg");
    background-position: center;
    background-size: cover;
    padding-top: 100px;
    padding-bottom: 200px;
  }
  .nome {
    background-color: rgb(123, 203, 206, 0.3);
    padding: 1px 12px;
    border-radius: 5px;
    font-weight: bold;
  }

  .feedback-card {
    border-radius: 10px;
    background-color: $shark;
    height: 230px;
    margin-bottom: 90px;
  }

  .title ul {
    list-style: disc;
  }
  .fa-gem {
    color: $bluelagoon;
  }
  .contacts-icons {
    color: $bluelagoon;
    background-color: $seanymph;
    border-radius: 50%;
    height: 20px;
    width: 20px;
    padding: 10px;
  }

  .form-color {
    background-color: #ececec;
  }

  .below-footer{
    height: 40px;
    background-color: rgb(8, 8, 8);
}
</style>
