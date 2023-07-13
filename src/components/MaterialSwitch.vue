<template>
  <div class="form-check form-switch d-flex">
    <input
      class="form-check-input"
      :class="inputClass"
      type="checkbox"
      :name="name"
      :id="id"
      :checked="checked"
    />
    <label class="form-check-label ms-3" :class="labelClass" :for="id">
      <slot />
    </label>
  </div>
</template>

<script>
export default {
  name: "MaterialSwitch",
  props: {
    name: String,
    id: String,
    checked: String,
    labelClass: String,
    inputClass: String,
  },
};
</script>
