<template>
  <div class="form-check p-0">
    <input
      class="form-check-input"
      type="checkbox"
      :name="name"
      :id="id"
      :checked="checked"
    />
    <label :for="id" class="custom-control-label">
      <slot />
    </label>
  </div>
</template>

<script>
export default {
  name: "MaterialCheckbox",
  props: {
    name: String,
    id: String,
    checked: String,
  },
};
</script>
