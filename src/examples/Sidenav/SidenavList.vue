<template>
  <div
    class="w-auto h-auto collapse navbar-collapse max-height-vh-100 h-100"
    id="sidenav-collapse-main"
  >
    <ul class="navbar-nav">
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="dashboard"
          navText="Dashboard"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">dashboard</i>
          </template>
        </sidenav-collapse>
      </li>
      <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="tables"
          navText="Tables"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">table_view</i>
          </template>
        </sidenav-collapse>
      </li>
      <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="billing"
          navText="Billing"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">receipt_long</i>
          </template>
        </sidenav-collapse>
      </li>
       <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="rtl-page"
          navText="Rtl"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">format_textdirection_r_to_l</i>
          </template>
        </sidenav-collapse>
      </li>
       <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="notifications"
          navText="Notifications"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">notifications</i>
          </template>
        </sidenav-collapse>
      </li>
      <li class="mt-3 nav-item">
        <h6
          class="text-xs ps-4 text-uppercase font-weight-bolder text-white"
          :class="this.$store.state.isRTL ? 'me-4' : 'ms-2'"
        >
         ACCOUNT PAGES
        </h6>
      </li>
      <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="profile"
          navText="Profile"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">person</i>
          </template>
        </sidenav-collapse>
      </li>
     <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="sign-in"
          navText="SignIn"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">login</i>
          </template>
        </sidenav-collapse>
      </li>
      <li class="nav-item">
        <sidenav-collapse
        url="#"
        :aria-controls="''"
        v-bind:collapse="false"
          collapseRef="sign-up"
          navText="SignUp"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">assignment</i>
          </template>
        </sidenav-collapse>
      </li>
    
    </ul>
  </div>
</template>
<script>
import SidenavCollapse from "./SidenavCollapse.vue";

export default {
  name: "SidenavList",
  props: {
    cardBg: String,
  },
  data() {
    return {
      title: "Soft UI Dashboard PRO",
      controls: "dashboardsExamples",
      isActive: "active",
    };
  },
  components: {
    SidenavCollapse,
  },
  methods: {
    getRoute() {
      const routeArr = this.$route.path.split("/");
      return routeArr[1];
    },
  },
};
</script>
