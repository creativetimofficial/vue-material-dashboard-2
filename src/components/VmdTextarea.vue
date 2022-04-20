<template>
  <div
    class="input-group"
    :class="`input-group-${variant} ${getStatus(error, success)}`"
  >
    <textarea
      :id="id"
      class="form-control"
      :rows="rows"
      :name="name"
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
  name: "VmdTextarea",
  props: {
    variant: {
      type: String,
      default: "outline",
    },
    id: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      default: "",
    },
    value: {
      type: String,
      default: "",
    },
    placeholder: {
      type: String,
      default: "Your text here...",
    },
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
  mounted() {
    setMaterialInput();
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
};
</script>
