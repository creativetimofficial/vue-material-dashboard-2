<template>
  <div
    class="w-auto h-auto collapse navbar-collapse max-height-vh-100 h-100"
    id="sidenav-collapse-main"
  >
    <ul class="navbar-nav">
      <li class="nav-item">
        <router-link :to="{ name: 'Dashboard' }">
          <sidenav-collapse collapseRef="dashboard" navText="Dashboard">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">dashboard</i>
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link :to="{ name: 'Tables' }">
          <sidenav-collapse collapseRef="tables" navText="Tables">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">table_view</i>
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link :to="{ name: 'Billing' }">
          <sidenav-collapse collapseRef="billing" navText="Billing">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">receipt_long</i>
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link :to="{ name: 'RTL' }">
          <sidenav-collapse collapseRef="rtl-page" navText="Rtl">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5"
                >format_textdirection_r_to_l</i
              >
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link :to="{ name: 'Notifications' }">
          <sidenav-collapse collapseRef="notifications" navText="Notifications">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">notifications</i>
            </template>
          </sidenav-collapse>
        </router-link>
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
        <router-link :to="{ name: 'Profile' }">
          <sidenav-collapse collapseRef="profile" navText="Profile">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">person</i>
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link :to="{ name: 'SignIn' }">
          <sidenav-collapse collapseRef="sign-in" navText="SignIn">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">login</i>
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
      <li class="nav-item">
        <router-link :to="{ name: 'SignUp' }">
          <sidenav-collapse collapseRef="sign-up" navText="SignUp">
            <template v-slot:icon>
              <i class="material-icons-round opacity-10 fs-5">assignment</i>
            </template>
          </sidenav-collapse>
        </router-link>
      </li>
    </ul>
    <div class="sidenav-footer position-absolute w-100 bottom-0">
      <div class="mx-3">
        <a
          class="btn mt-4 w-100"
          :class="`bg-gradient-${this.$store.state.mcolor}`"
          href="https://www.creative-tim.com/product/vue-material-dashboard-2-pro"
          type="button"
          >Upgrade to pro</a
        >
      </div>
    </div>
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
};
</script>
