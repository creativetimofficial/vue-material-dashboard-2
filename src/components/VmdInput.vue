<template>
  <div
    class="input-group"
    :class="`input-group-${variant} ${getStatus(error, success)}`"
  >
    <label :class="variant === 'static' ? '' : 'form-label'">{{ label }}</label>
    <input
      :type="type"
      class="form-control"
      :class="getClasses(size)"
      :name="name"
      :id="id"
      :value="value"
      :placeholder="placeholder"
      :isRequired="isRequired"
      :disabled="disabled"
    />
  </div>
</template>

<script>
import setMaterialInput from "@/assets/js/material-input.js";

export default {
  name: "vmd-input",
  props: {
    variant: {
      type: String,
      default: "outline",
    },
    label: String,
    size: {
      type: String,
      default: "default",
    },
    success: {
      type: Boolean,
      default: false,
    },
    error: {
      type: Boolean,
      default: false,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
    name: String,
    id: String,
    value: String,
    placeholder: String,
    type: {
      type: String,
      default: "text",
    },
    isRequired: Boolean,
  },
  methods: {
    getClasses: (size) => {
      let sizeValue;

      sizeValue = size ? `form-control-${size}` : null;

      return sizeValue;
    },
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
