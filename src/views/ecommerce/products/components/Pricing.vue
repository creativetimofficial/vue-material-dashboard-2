<template>
  <div
    class="pt-3 bg-white multisteps-form__panel border-radius-xl"
    data-animation="FadeIn"
  >
    <h5 class="font-weight-bolder">Pricing</h5>
    <div class="mt-3 multisteps-form__content">
      <div class="row">
        <div class="col-3">
          <vmd-input variant="dynamic" label="Price" />
        </div>
        <div class="col-4">
          <select
            class="form-control"
            name="choices-sizes"
            id="choices-currency"
          >
            <option value="Choice 1" selected>USD</option>
            <option value="Choice 2">EUR</option>
            <option value="Choice 3">GBP</option>
            <option value="Choice 4">CNY</option>
            <option value="Choice 5">INR</option>
            <option value="Choice 6">BTC</option>
          </select>
        </div>
        <div class="col-5">
          <vmd-input variant="dynamic" label="SKU" />
        </div>
      </div>
      <div class="row">
        <div class="col-12">
          <label class="mt-4 ms-0 form-label">Tags</label>
          <select
            class="form-control"
            name="choices-tags"
            id="choices-tags"
            multiple
          >
            <option value="Choice 1" selected>In Stock</option>
            <option value="Choice 2">Out of Stock</option>
            <option value="Choice 3">Sale</option>
            <option value="Choice 4">Black Friday</option>
          </select>
        </div>
      </div>
      <div class="mt-4 button-row d-flex col-12">
        <vmd-button
          type="button"
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
          >Next</vmd-button
        >
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable prettier/prettier */
import Choices from "choices.js";
import VmdButton from "@/components/VmdButton.vue";
import VmdInput from "@/components/VmdInput.vue";

export default {
  name: "pricing",
  components: {
    VmdButton,
    VmdInput,
  },
  mounted() {
    if (document.getElementById("choices-currency")) {
      let element = document.getElementById("choices-currency");
      new Choices(element, {
        searchEnabled: false,
      });
    }

    if (document.getElementById("choices-tags")) {
      var tags = document.getElementById("choices-tags");
      const examples = new Choices(tags, {
        removeItemButton: true,
      });

      examples.setChoices(
        [
          {
            value: "One",
            label: "Expired",
            disabled: true,
          },
          {
            value: "Two",
            label: "Out of Stock",
            selected: true,
          },
        ],
        "value",
        "label",
        false,
      );
    }
  },
};
</script>
