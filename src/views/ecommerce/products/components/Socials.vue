<template>
  <div
    class="pt-3 bg-white multisteps-form__panel border-radius-xl"
    data-animation="FadeIn"
  >
    <h5 class="font-weight-bolder">Socials</h5>
    <div class="multisteps-form__content">
      <div class="mt-3 row">
        <div class="col-12">
          <vmd-input label="Shopify Handle" variant="dynamic" />
        </div>
        <div class="col-12 mt-3">
          <vmd-input label="Facebook Handle" variant="dynamic" />
        </div>
        <div class="col-12 mt-3">
          <vmd-input label="Instagram Handle" variant="dynamic" />
        </div>
      </div>
      <div class="row">
        <div class="mt-4 button-row d-flex col-12">
          <vmd-button
            color="secondary"
            variant="gradient"
            class="mb-0 js-btn-prev"
            title="Prev"
            @click="this.$parent.prevStep"
            >Prev</vmd-button
          >
          <vmd-button
            type="button"
            color="dark"
            variant="gradient"
            class="mb-0 ms-auto js-btn-next"
            title="Next"
            @click="this.$parent.nextStep"
            >Next</vmd-button
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VmdInput from "@/components/VmdInput.vue";
import VmdButton from "@/components/VmdButton.vue";

export default {
  name: "socials",
  components: {
    VmdInput,
    VmdButton,
  },
};
</script>
