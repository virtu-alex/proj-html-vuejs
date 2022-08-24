<template>
  <div>
    <!-- WHO WE ARE SECTION -->
    <section class="who-we-are">
      <div class="container">
        <div class="row">
          <div class="col-8 title">
            <h5 class="presentation">WHO WE ARE</h5>
            <h1>Excellence in Transport</h1>
            <p class="py-2 text-secondary">
              {{ lorem }}
            </p>
            <p class="py-3 text-secondary">
              {{ lorem }}
            </p>
            <p class="py-3 comment">
              {{ lorem }}
            </p>
            <p class="py-3 text-secondary">
              {{ halfLorem }}
            </p>
            <ul class="text-secondary">
              <li>Lorem ipsum dolor sit amet</li>
              <li>consectetur adipisicing elit</li>
              <li>Non quam, sit nam vel</li>
              <li>dolor sit amet consectetur adipisicing elit</li>
              <li>sunt quod natus veritatis tempore fugit</li>
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
          <div class="col-9">
            <h5 class="presentation">ROAD TRANSPORT</h5>
            <h2><strong>Main</strong> <strong>Services</strong></h2>
            <p>
              {{ expertiseText }}
            </p>
          </div>
          <div class="col-3">
            <BaseButton />
          </div>
        </div>
        <div class="row">
          <div class="col-4">component</div>
          <div class="col-4">component</div>
          <div class="col-4">component</div>
        </div>
      </div>
    </section>
    <!-- LOGISTICAL SECTION -->
    <section id="process" class="logistical pt-5">
      <div class="row justify-content-center">
        <div class="col-8 text-center">
          <h5>How it Works in practice</h5>
          <h1>Logistical Procedure</h1>
          <p>
            We Work with innovative methodologies to ensure that the entire
            delivery process is done from start to finish as planned.
          </p>
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-2">
          <h5>Collection of information</h5>
          <p>{{ halfLorem }}</p>
        </div>
        <div class="col-2">
          <h5>Collection of information</h5>
          <p>{{ halfLorem }}</p>
        </div>
        <div class="col-2">
          <h5>Collection of information</h5>
          <p>{{ halfLorem }}</p>
        </div>
        <div class="col-2">
          <h5>Collection of information</h5>
          <p>{{ halfLorem }}</p>
        </div>
        <div class="col-2">
          <h5>Collection of information</h5>
          <p>{{ halfLorem }}</p>
        </div>
      </div>
    </section>
    <!-- RESULTS SECTION -->
    <section id="testimonials" class="results text-white">
      <div class="container">
        <div class="row">
          <div class="col">
            <h5>What are we doing</h5>
            <h1>Results in Numbers</h1>
          </div>
          <div class="row pt-5 text-center">
            <div class="col-3">
              <h3>128</h3>
              <p>Certifications</p>
            </div>
            <div class="col-3">
              <h3>230</h3>
              <p>Employees</p>
            </div>
            <div class="col-3">
              <h3>517</h3>
              <p>Customers</p>
            </div>
            <div class="col-3">
              <h3>94</h3>
              <p>Countries Served</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- TRUSTED FEEDBACK SECTION -->
    <section class="feedback bg-dark text-white">
      <div class="container pt-5">
        <div class="row justify-content-center">
          <div class="col-8 text-center">
            <h5>Curstomer testimonials</h5>
            <h1>Trusted Feedback</h1>
            <p>
              We Work intensively in search of ideals that can add up in the
              lives of our curstomers. This is what moves us and we are grateful
              for the recognition.
            </p>
          </div>
        </div>
        <div class="row justify-content-center">
          <div class="col p-2 feedback-card">
            <img
              :src="require('@/assets/Images/logo-1.png')"
              alt="WooCommerce"
            />
            <p>{{ feedbackText }}</p>
          </div>
          <div class="col mx-3 p-2 feedback-card">
            <img :src="require('@/assets/Images/logo-2.png')" alt="WordPress" />
            <p>{{ feedbackText }}</p>
          </div>
          <div class="col p-2 feedback-card">
            <img :src="require('@/assets/Images/logo-3.png')" alt="Pingdom" />
            <p>{{ feedbackText }}</p>
          </div>
        </div>
      </div>
    </section>
    <!-- SEND A MESSAGE SECTION -->
    <section class="send-message">
      <div class="container pt-5">
        <div class="row">
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
              <li class="py-3">
                <font-awesome-icon
                  class="phone px-2"
                  icon="fa-solid fa-phone"
                />
                <span>{{ phone }}</span>
              </li>
              <li class="py-3">
                <font-awesome-icon
                  class="mail px-2"
                  icon="fa-solid fa-envelope"
                />
                <span>{{ mail }}</span>
              </li>
              <li class="py-3">
                <font-awesome-icon
                  class="street px-2"
                  icon="fa-solid fa-envelope"
                />
                <span>{{ street }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
    <section class="footer bg-dark py-5 text-white">
      <div class="container">
        <div class="">
          <div class="col-3">
            <ul>
              <li>
                <BaseLogo />
              </li>
              <li>A Functional HTML Template for Corporate & Business.</li>
              <li>{{ phone }}</li>
              <li>{{ mail }}</li>
              <li>{{ street }}</li>
              <li><BaseButton /></li>
            </ul>
          </div>
          <div class="col-3"></div>
          <div class="col-3"></div>
          <div class="col-3"></div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  import BaseButton from "./BaseButton.vue";
  import BaseLogo from "./BaseLogo.vue";
  import BaseForm from "./BaseForm.vue";
  import data from "../data";
  import VehicleTypes from "./VehicleTypes.vue";
  import {library} from "@fortawesome/fontawesome-svg-core";

  /* import font awesome icon component */
  import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";

  /* import specific icons */
  import {faPhone, faEnvelope} from "@fortawesome/free-solid-svg-icons";

  /* add icons to the library */
  library.add(faPhone, faEnvelope);
  export default {
    name: "BaseMain",
    components: {
      VehicleTypes,
      BaseButton,
      FontAwesomeIcon,
      BaseForm,
      BaseLogo,
    },
    data() {
      return {...data};
    },
  };
</script>
<style lang="scss">
  .who-we-are {
    padding-top: 100px;
    padding-bottom: 100px;
  }

  .presentation {
    color: #52bbbb;
  }

  .comment {
    border-left: 4px solid rgb(96, 157, 159, 0.4);
    padding-left: 20px;
    font-style: italic;
    color: grey;
  }

  .results {
    background-image: url("/src/assets/Images/bg-10.jpg");
    background-size: cover;
    padding-top: 80px;
    padding-bottom: 200px;
  }

  .feedback-card {
    background-color: #69696d;
    width: calc(90% / 3);
  }
  .title ul {
    list-style: disc;
  }

  .phone {
    background-color: aqua;
    border-radius: 50%;
  }

  .mail {
    background-color: aqua;
    border-radius: 50%;
  }

  .street {
    background-color: aqua;
    border-radius: 50%;
  }

  .form-color {
    background-color: #ececec;
  }
</style>
