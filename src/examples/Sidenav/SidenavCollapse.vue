<template>
  <router-link
    :data-bs-toggle="collapse ? 'collapse' : ''"
    :to="collapse ? `#${collapseRef}` : collapseRef"
    :aria-controls="collapseRef"
    :aria-expanded="isExpanded"
    class="nav-link"
    :class="getRoute() === collapseRef ? `active bg-gradient-${color}` : ''"
    v-bind="$attrs"
    type="button"
    @click="isExpanded = !isExpanded"
  >
    <div
      class="text-center d-flex align-items-center justify-content-center"
      :class="isRTL ? ' ms-2' : 'me-2'"
    >
      <slot name="icon"></slot>
    </div>
    <span class="nav-link-text" :class="isRTL ? ' me-1' : 'ms-1'">{{
      navText
    }}</span>
  </router-link>
  <div :class="isExpanded ? 'collapse show' : 'collapse'">
    <slot name="list"></slot>
  </div>
</template>
<script>
import { mapState } from "vuex";

export default {
  name: "SidenavCollapse",
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
  computed: {
    ...mapState(["isRTL", "color"]),
  },
};
</script>
