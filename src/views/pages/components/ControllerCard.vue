<template>
  <div class="card blur shadow-blur">
    <div class="card-body">
      <div class="d-flex">
        <p class="mb-0" :class="this.$store.state.isRTL ? 'ms-5' : 'me-5'">
          {{ controllerIs }}
        </p>
        <vmd-switch checked />
      </div>
      <img
        class="img-fluid pt-3 pb-2"
        src="../../../assets/img/small-logos/icon-bulb.svg"
        alt="bulb_icon"
      />
      <p class="mb-0">{{ text }}</p>
    </div>
  </div>
</template>

<script>
import VmdSwitch from "@/components/VmdSwitch.vue";

export default {
  name: "controller-card",
  components: {
    VmdSwitch,
  },
  props: {
    controllerIs: {
      type: String,
      default: "On",
    },
    text: {
      type: String,
      default: "Lights",
    },
  },
};
</script>
