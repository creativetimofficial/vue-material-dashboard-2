<template>
  <li class="nav-item active">
    <router-link class="nav-link" :to="to">
      <span class="sidenav-mini-icon text-white"> {{ miniIcon }} </span>
      <span class="sidenav-normal me-3 ms-3 ps-1 text-white text-white">
        {{ text }}
      </span>
    </router-link>
  </li>
</template>
<script>
export default {
  name: "sidenav-item",
  props: {
    to: {
      type: [Object, String],
      required: true,
    },
    miniIcon: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
  },
};
</script>
