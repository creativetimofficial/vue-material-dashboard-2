<template>
  <div class="mb-3 timeline-block">
    <span class="timeline-step p-3" :class="`bg-${color}`">
      <i class="material-icons opacity-10" :class="icon.class">{{
        icon.component
      }}</i>
    </span>
    <div class="timeline-content">
      <h6
        class="mb-0 text-sm font-weight-bold"
        :class="$parent.darkMode ? 'text-white' : 'text-dark'"
      >
        {{ title }}
      </h6>
      <p class="mt-1 mb-0 text-xs text-secondary font-weight-normal">
        {{ dateTime }}
      </p>
      <p
        v-if="description"
        class="mt-3 mb-2 text-sm"
        :class="$parent.darkMode ? 'text-white' : 'text-dark'"
      >
        {{ description }}
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "TimelineItem",
  props: {
    color: {
      type: String,
      default: "",
    },
    icon: {
      type: Object,
      component: String,
      class: String,
      default: () => {},
    },
    title: {
      type: String,
      default: "",
    },
    dateTime: {
      type: String,
      default: "",
    },
    description: {
      type: String,
      default: "",
    },
  },
};
</script>
