<template>
  <div class="card mb-2" :class="directionReverse ? reverseDirection : ''">
    <div class="card-header p-3 pt-2">
      <div
        class="icon icon-lg icon-shape shadow-dark shadow text-center border-radius-xl mt-n4 position-absolute"
        :class="iconBackground"
      >
        <i
          class="material-icons opacity-10"
          :class="iconClass"
          aria-hidden="true"
          >{{ iconName }}</i
        >
      </div>
      <div class="text-end pt-1" >
        <p class="text-sm mb-0 text-capitalize">{{ title }}</p>
        <h4 class="mb-0">{{ value }}</h4>
      </div>
    </div>
    <hr class="dark horizontal my-0" />
    <div class="card-footer p-3">
      <p class="mb-0">
        <span class="text-success text-sm font-weight-bolder">{{
          percentage
        }}</span>
        {{ detail }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "mini-cards",
  data() { 
    return {
      reverseDirection: "flex-row-reverse justify-content-between"
    }
  },
  props: {
    directionReverse: Boolean,
    title: {
      type: String,
      required: true,
    },
    detail: {
      type: String,
      required: true,
    },
    value: {
      required: true,
    },
    percentage: String,
    iconName: {
      type: String,
      required: true,
    },
    iconClass: {
      type: String,
      required: true,
    },
    iconBackground: {
      type: String,
      default: "bg-white",
    },
  },
};
</script>
