<template>
  <div
    class="pt-3 bg-white multisteps-form__panel js-active position-relative"
    data-animation="FadeIn"
  >
    <div class="text-center row">
      <div class="mx-auto col-10">
        <h5 class="font-weight-normal">
          Let's start with the basic information
        </h5>
        <p>
          Let us know your name and email address. Use an address you don't mind
          other users contacting you at
        </p>
      </div>
    </div>
    <div class="multisteps-form__content">
      <div class="mt-3 row">
        <div class="col-12 col-sm-4">
          <div class="avatar avatar-xxl position-relative">
            <img
              src="@/assets/img/team-2.jpg"
              class="border-radius-md"
              alt="team-2"
            />
            <a
              href="javascript:;"
              class="btn btn-sm btn-icon-only bg-gradient-success position-absolute bottom-0 end-0 mb-n2 me-n2 d-grid"
            >
              <span
                class="material-icons text-xs top-0"
                data-bs-toggle="tooltip"
                data-bs-placement="top"
                title
                aria-hidden="true"
                data-bs-original-title="Edit Image"
                aria-label="Edit Image"
                >edit</span
              >
            </a>
          </div>
        </div>
        <div class="mt-4 col-12 col-sm-8 mt-sm-0 text-start">
          <div class="d-block mb-4">
            <vmd-input variant="dynamic" label="First Name" />
          </div>
          <div class="d-block mb-4">
            <vmd-input variant="dynamic" label="Last Name" />
          </div>
          <div class="d-block mb-4">
            <vmd-input type="email" variant="dynamic" label="Email Address" />
          </div>
        </div>
      </div>
      <div class="mt-4 button-row d-flex">
        <button
          class="mb-0 btn bg-gradient-dark ms-auto js-btn-next"
          type="button"
          title="Next"
          @click="this.$parent.nextStep"
        >
          Next
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import setTooltip from "@/assets/js/tooltip.js";
import VmdInput from "@/components/VmdInput.vue";

export default {
  name: "about",
  components: { VmdInput },
  mounted() {
    setTooltip();
  },
};
</script>
