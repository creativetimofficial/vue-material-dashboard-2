<template>
  <aside
    id="sidenav-main"
    class="sidenav navbar navbar-vertical navbar-expand-xs border-0 border-radius-xl my-3 ms-3"
    :class="`${
      $store.state.isRTL ? 'me-3 rotate-caret fixed-end' : 'fixed-start ms-3'
    } ${$store.state.sidebarType}`"
  >
    <div class="sidenav-header">
      <i
        class="top-0 p-3 cursor-pointer fas fa-times text-secondary opacity-5 position-absolute end-0 d-none d-xl-none"
        aria-hidden="true"
        id="iconSidenav"
      ></i>
      <a class="m-0 navbar-brand" href="/">
        <img
          :src="
            $store.state.sidebarType === 'bg-white' ||
            ($store.state.sidebarType === 'bg-transparent' &&
              !$store.state.isDarkMode)
              ? logoDark
              : logo
          "
          class="navbar-brand-img h-100"
          alt="main_logo"
        />
        <span class="ms-2 font-weight-bold text-white"
          >Material Dashboard 2</span
        >
      </a>
    </div>
    <hr class="horizontal light mt-0 mb-2" />
    <sidenav-list />
  </aside>
</template>
<script>
import SidenavList from "./SidenavList.vue";
import logo from "@/assets/img/logo-ct.png";
import logoDark from "@/assets/img/logo-ct-dark.png";

export default {
  name: "index",
  components: {
    SidenavList,
  },
  data() {
    return {
      logo,
      logoDark,
    };
  },
  props: ["custom_class"],
};
</script>
