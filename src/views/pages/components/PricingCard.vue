<template>
  <div class="card shadow-lg" :class="premium ? 'bg-gradient-dark' : ''">
    <span
      class="badge rounded-pill w-30 mt-n2 mx-auto"
      :class="premium ? 'bg-gradient-success text-white' : 'bg-light text-dark'"
      >{{ mPackage }}</span
    >
    <div class="card-header text-center pt-4 pb-3 bg-transparent">
      <h1
        class="font-weight-bold mt-2"
        :class="premium ? 'text-white' : 'text-dark'"
      >
        <small class="text-lg align-top me-1">$</small>{{ value
        }}<small class="text-lg">/mo</small>
      </h1>
    </div>
    <div
      class="card-body text-lg-start text-center pt-0"
      :class="premium ? 'text-white' : 'text-dark'"
    >
      <div class="p-2 d-flex justify-content-lg-start justify-content-center">
        <i class="material-icons my-auto">done</i>
        <span class="ps-3">{{ numOfMembers }} team members</span>
      </div>
      <div class="p-2 d-flex justify-content-lg-start justify-content-center">
        <i class="material-icons">done</i>
        <span class="ps-3">{{ storage }}GB Cloud storage</span>
      </div>
      <div class="p-2 d-flex justify-content-lg-start justify-content-center">
        <i class="material-icons">{{ intHelp ? "done" : "remove" }}</i>
        <span class="ps-3">Integration help</span>
      </div>
      <div class="p-2 d-flex justify-content-lg-start justify-content-center">
        <i class="material-icons">{{ skFiles ? "done" : "remove" }}</i>
        <span class="ps-3">Sketch Files</span>
      </div>
      <div class="p-2 d-flex justify-content-lg-start justify-content-center">
        <i class="material-icons">{{ apiAccess ? "done" : "remove" }}</i>
        <span class="ps-3">API Access</span>
      </div>
      <div class="p-2 d-flex justify-content-lg-start justify-content-center">
        <i class="material-icons">{{ comDocument ? "done" : "remove" }}</i>
        <span class="ps-3">Complete documentation</span>
      </div>
      <a
        href="javascript:;"
        class="mt-3 mb-0 btn btn-icon d-lg-block"
        :class="premium ? 'bg-gradient-success' : 'bg-gradient-dark'"
      >
        {{ btnValue }}
        <i class="fas fa-arrow-right ms-1"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "pricing-card",
  props: {
    mPackage: {
      type: String,
      default: "Starter",
    },
    value: {
      type: String,
      default: "59",
    },
    btnValue: {
      type: String,
      default: "59",
    },
    numOfMembers: {
      type: String,
      default: "2",
    },
    storage: {
      type: String,
      default: "20",
    },
    intHelp: {
      type: Boolean,
      default: false,
    },
    skFiles: {
      type: Boolean,
      default: false,
    },
    apiAccess: {
      type: Boolean,
      default: false,
    },
    comDocument: {
      type: Boolean,
      default: false,
    },
    premium: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
