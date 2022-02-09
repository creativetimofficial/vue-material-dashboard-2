<template>
  <div
    class="multisteps-form__panel border-radius-xl bg-white"
    data-animation="FadeIn"
  >
    <h5 class="font-weight-bolder">Socials</h5>
    <p class="mb-0 text-sm">Please provide at least one social link</p>
    <div class="multisteps-form__content">
      <div class="row mt-3">
        <div class="col-12">
          <vmd-input label="Twitter Handle" variant="dynamic" />
        </div>
        <div class="col-12 mt-3">
          <vmd-input label="Facebook Handle" variant="dynamic" />
        </div>
        <div class="col-12 mt-3">
          <vmd-input label="Instagram Handle" variant="dynamic" />
        </div>
      </div>
      <div class="button-row d-flex mt-4">
        <vmd-button
          type="button"
          color="light"
          variant="gradient"
          class="js-btn-prev"
          @click="this.$parent.prevStep"
          >Prev</vmd-button
        >
        <vmd-button
          type="button"
          color="dark"
          variant="gradient"
          class="ms-auto js-btn-next"
          @click="this.$parent.nextStep"
          >Next</vmd-button
        >
      </div>
    </div>
  </div>
</template>

<script>
import VmdButton from "@/components/VmdButton.vue";
import VmdInput from "@/components/VmdInput.vue";

export default {
  name: "socials",
  components: {
    VmdButton,
    VmdInput,
  },
};
</script>
