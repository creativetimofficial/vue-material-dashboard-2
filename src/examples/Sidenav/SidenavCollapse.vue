<template>
  <a
    :data-bs-toggle="collapse ? 'collapse' : ''"
    :href="collapse ? `#${collapseRef}` : collapseRef"
    :aria-controls="collapseRef"
    :aria-expanded="isExpanded"
    class="nav-link"
    :class="
      getRoute() === collapseRef
        ? `active bg-gradient-${$store.state.mcolor}`
        : ''
    "
    v-bind="$attrs"
    type="button"
    @click="isExpanded = !isExpanded"
  >
    <div
      class="text-center d-flex align-items-center justify-content-center"
      :class="$store.state.isRTL ? ' ms-2' : 'me-2'"
    >
      <slot name="icon"></slot>
    </div>
    <span
      class="nav-link-text"
      :class="$store.state.isRTL ? ' me-1' : 'ms-1'"
      >{{ navText }}</span
    >
  </a>
  <div :class="isExpanded ? 'collapse show' : 'collapse'">
    <slot name="list"></slot>
  </div>
</template>
<script>
export default {
  name: "sidenav-collapse",
  props: {
    collapseRef: {
      type: String,
      required: true,
    },
    navText: {
      type: String,
      required: true,
    },
    collapse: {
      type: Boolean,
      default: true,
    },
  },
  data() {
    return {
      isExpanded: false,
    };
  },
  methods: {
    getRoute() {
      const routeArr = this.$route.path.split("/");
      return routeArr[1];
    },
  },
};
</script>
