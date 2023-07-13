<template>
  <div
    class="input-group"
    :class="`input-group-${variant} ${getStatus(error, success)}`"
  >
    <textarea
      class="form-control"
      :rows="rows"
      :name="name"
      :id="id"
      :value="value"
      :placeholder="placeholder"
      :isRequired="isRequired"
      :disabled="disabled"
    ></textarea>
  </div>
</template>

<script>
import setMaterialInput from "@/assets/js/material-input.js";

export default {
  name: "MaterialTextarea",
  props: {
    variant: {
      type: String,
      default: "outline",
    },
    id: String,
    name: String,
    value: String,
    placeholder: String,
    isRequired: Boolean,
    disabled: {
      type: Boolean,
      default: false,
    },
    rows: {
      type: Number,
      default: 5,
    },
    success: {
      type: Boolean,
      default: false,
    },
    error: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    getStatus: (error, success) => {
      let isValidValue;

      if (success) {
        isValidValue = "is-valid";
      } else if (error) {
        isValidValue = "is-invalid";
      } else {
        isValidValue = null;
      }

      return isValidValue;
    },
  },
  mounted() {
    setMaterialInput();
  },
};
</script>
