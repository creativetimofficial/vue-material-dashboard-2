<template>
  <div
    class="multisteps-form__panel border-radius-xl bg-white"
    data-animation="FadeIn"
  >
    <h5 class="font-weight-bolder">Address</h5>
    <div class="multisteps-form__content">
      <div class="row mt-3">
        <div class="col">
          <vmd-input label="Address 1" variant="dynamic" />
        </div>
      </div>
      <div class="row mt-3">
        <div class="col">
          <vmd-input label="Address 2" variant="dynamic" />
        </div>
      </div>
      <div class="row mt-3">
        <div class="col-12 col-sm-6">
          <vmd-input label="City" variant="dynamic" />
        </div>
        <div class="col-6 col-sm-3 mt-3 mt-sm-0">
          <select
            class="multisteps-form__select form-control"
            name="choices-state"
            id="choices-state"
          >
            <option selected="selected">...</option>
            <option value="1">State 1</option>
            <option value="2">State 2</option>
          </select>
        </div>
        <div class="col-6 col-sm-3 mt-3 mt-sm-0">
          <vmd-input label="Zip" variant="dynamic" />
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
import VmdInput from "@/components/VmdInput.vue";
import VmdButton from "@/components/VmdButton.vue";
import Choices from "choices.js";

export default {
  name: "address",
  components: {
    VmdInput,
    VmdButton,
  },
  mounted() {
    if (document.getElementById("choices-state")) {
      var element = document.getElementById("choices-state");
      new Choices(element, {
        searchEnabled: false,
      });
    }
  },
};
</script>

<style></style>
