<template>
  <div class="py-4 container-fluid">
    <div class="row min-vh-80">
      <div class="col-lg-8 col-md-10 col-12 m-auto">
        <h3 class="mt-3 mb-0 text-center">Add new Product</h3>
        <p class="lead font-weight-normal opacity-8 mb-7 text-center">
          This information will let us know more about you.
        </p>
        <div class="card">
          <div class="card-header p-0 position-relative mt-n5 mx-3 z-index-2">
            <div
              class="bg-gradient-success shadow-success border-radius-lg pt-4 pb-3"
            >
              <div class="multisteps-form__progress">
                <button
                  class="multisteps-form__progress-btn js-active"
                  type="button"
                  title="Product Info"
                  @click="activeStep = 0"
                  :class="activeStep >= 0 ? activeClass : ''"
                >
                  <span>1. Product Info</span>
                </button>
                <button
                  class="multisteps-form__progress-btn"
                  type="button"
                  title="Media"
                  @click="activeStep = 1"
                  :class="activeStep >= 1 ? activeClass : ''"
                >
                  2. Media
                </button>
                <button
                  class="multisteps-form__progress-btn"
                  type="button"
                  title="Socials"
                  @click="activeStep = 2"
                  :class="activeStep >= 2 ? activeClass : ''"
                >
                  3. Socials
                </button>
                <button
                  class="multisteps-form__progress-btn"
                  type="button"
                  title="Pricing"
                  @click="activeStep = 3"
                  :class="activeStep >= 3 ? activeClass : ''"
                >
                  4. Pricing
                </button>
              </div>
            </div>
          </div>
          <div class="card-body">
            <form class="multisteps-form__form">
              <!--single form panel-->
              <product-info :class="activeStep === 0 ? activeClass : ''" />
              <!--single form panel-->
              <media :class="activeStep === 1 ? activeClass : ''" />
              <!--single form panel-->
              <socials :class="activeStep === 2 ? activeClass : ''" />
              <!--single form panel-->
              <pricing :class="activeStep === 3 ? activeClass : ''" />
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProductInfo from "./components/ProductInfo.vue";
import Media from "./components/Media.vue";
import Socials from "./components/Socials.vue";
import Pricing from "./components/Pricing.vue";

import setNavPills from "@/assets/js/nav-pills.js";
export default {
  name: "profile-overview",
  data() {
    return {
      showMenu: false,
      activeClass: "js-active position-relative",
      activeStep: 0,
      formSteps: 3,
    };
  },
  components: {
    ProductInfo,
    Media,
    Socials,
    Pricing,
  },
  methods: {
    nextStep() {
      if (this.activeStep < this.formSteps) {
        this.activeStep += 1;
        console.log(this.activeStep);
      } else {
        this.activeStep -= 1;
        console.log(this.activeStep);
      }
    },
    prevStep() {
      if (this.activeStep > 0) {
        this.activeStep -= 1;
        console.log(this.activeStep);
      }
    },
  },
  mounted() {
    setNavPills();
  },
};
</script>
