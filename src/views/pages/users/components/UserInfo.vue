<template>
  <div
    class="multisteps-form__panel border-radius-xl bg-white"
    data-animation="FadeIn"
  >
    <h5 class="font-weight-bolder mb-0">About me</h5>
    <p class="mb-0 text-sm">Mandatory informations</p>
    <div class="multisteps-form__content">
      <div class="row mt-3">
        <div class="col-12 col-sm-6">
          <vmd-input label="First Name" variant="dynamic" />
        </div>
        <div class="col-12 col-sm-6 mt-3 mt-sm-0">
          <vmd-input label="Last Name" variant="dynamic" />
        </div>
      </div>
      <div class="row mt-3">
        <div class="col-12 col-sm-6">
          <vmd-input label="Company" variant="dynamic" />
        </div>
        <div class="col-12 col-sm-6 mt-3 mt-sm-0">
          <vmd-input type="email" label="Email Address" variant="dynamic" />
        </div>
      </div>
      <div class="row mt-3">
        <div class="col-12 col-sm-6">
          <vmd-input type="password" label="Password" variant="dynamic" />
        </div>
        <div class="col-12 col-sm-6 mt-3 mt-sm-0">
          <vmd-input
            type="password"
            label="Repeat Password"
            variant="dynamic"
          />
        </div>
      </div>
      <div class="button-row d-flex mt-4">
        <vmd-button
          type="button"
          color="dark"
          variant="gradient"
          class="ms-auto mb-0 js-btn-next"
          @click="this.$parent.nextStep"
          >Next</vmd-button
        >
      </div>
    </div>
  </div>
</template>

<script>
import VmdInput from "@/components/VmdInput.vue";
import VmdButton from "@/components/VmdButton.vue";

export default {
  name: "user-info",
  components: {
    VmdInput,
    VmdButton,
  },
};
</script>
