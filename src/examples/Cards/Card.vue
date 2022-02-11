<template>
  <div class="mb-4 card">
    <div class="p-3 card-body">
      <div class="row" :class="directionReverse ? reverseDirection : ''">
        <div :class="contentClass" class="col-8">
          <p class="mb-0 text-sm text-capitalize" :class="titleColor">
            {{ title }}
          </p>
          <h5 class="mb-0 font-weight-bolder" :class="valueColor">
            {{ value }}
            <span class="text-sm font-weight-bolder" :class="percentageColor">{{
              percentage
            }}</span>
          </h5>
        </div>
         <div class="col-4 text-end">
          <div
            class="icon icon-shape bg-gradient-success shadow text-center border-radius-md"
          >
            <i
              class="opacity-10 material-icons"
              :class="iconClass"
              aria-hidden="true"
              >{{ iconName }}</i
            >
          </div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "card",
  data() {
    return {
      reverseDirection: "flex-row-reverse justify-content-between",
    };
  },
  props: {
    directionReverse: Boolean,
    title: {
      type: String,
      required: true,
    },
    titleColor: {
      type: String,
    },
    value: {
      required: true,
    },
    valueColor: {
      type: String,
    },
    percentage: String,
    iconClass: {
      type: String,
      required: true,
    },
    percentageColor: {
      type: String,
      default: "text-success",
    },
    iconBackground: {
      type: String,
      default: "bg-white",
    },
    contentClass: {
      type: String,
    },
    iconName: {
      type: String,
      required: true,
    },
  },
};
</script>
