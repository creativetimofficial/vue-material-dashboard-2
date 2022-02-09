<template>
  <div class="card">
    <div class="card-body">
      <p>{{ title }}</p>
      <h3>{{ steps }}</h3>
      <vmd-badge color="success">+4.3%</vmd-badge>
    </div>
  </div>
</template>

<script>
import VmdBadge from "@/components/VmdBadge.vue";

export default {
  name: "steps-card",
  props: {
    title: {
      type: String,
      default: "Steps",
    },
    steps: {
      type: String,
      default: "11.4K",
    },
  },
  components: {
    VmdBadge,
  },
};
</script>
