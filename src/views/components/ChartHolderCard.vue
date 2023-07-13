<template>
  <div class="card z-index-2">
    <div
      class="card-header p-0 position-relative mt-n4 mx-3 z-index-2 bg-transparent"
    >
      <div
        class="border-radius-lg py-3 pe-1"
        :class="`bg-gradient-${color} shadow-${color}`"
      >
        <slot />
      </div>
    </div>
    <div class="card-body">
      <h6 class="mb-0">{{ title }}</h6>
      <!--  eslint-disable-next-line vue/no-v-html -->
      <p class="text-sm" v-html="subtitle"></p>
      <hr class="dark horizontal" />
      <div class="d-flex">
        <i class="material-icons text-sm my-auto me-1">schedule</i>
        <p class="mb-0 text-sm">{{ update }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChartHolderCard",
  props: {
    title: {
      type: String,
      default: "",
    },
    subtitle: {
      type: String,
      default: "",
    },
    update: {
      type: String,
      default: "",
    },
    color: {
      type: String,
      default: "primary",
    },
  },
};
</script>
