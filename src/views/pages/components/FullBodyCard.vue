<template>
  <div class="card">
    <div class="card-header pb-0">
      <div class="d-flex">
        <p>{{ title }}</p>
        <div :class="this.$store.state.isRTL ? 'me-auto' : 'ms-auto'">
          <vmd-badge color="success">{{ badgeText }}</vmd-badge>
        </div>
      </div>
    </div>
    <div class="card-body pt-0">
      <p class="mb-0">{{ description }}</p>
    </div>
  </div>
</template>

<script>
import VmdBadge from "@/components/VmdBadge.vue";

export default {
  name: "full-body-card",
  components: {
    VmdBadge,
  },
  props: {
    title: {
      type: String,
      default: "Full Body",
    },
    badgeText: {
      type: String,
      default: "Moderate",
    },
    description: {
      type: String,
      default:
        "What matters is the people who are sparked by it. And the people who are liked.",
    },
  },
};
</script>
