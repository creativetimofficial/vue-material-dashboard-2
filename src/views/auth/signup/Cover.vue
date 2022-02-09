<template>
  <navbar btnBackground="bg-gradient-success" />

  <main class="mt-0 main-content main-content-bg">
    <div
      class="page-header align-items-start min-height-300 m-3 border-radius-xl bg-gray-200"
      style="
        background-image: url('https://images.unsplash.com/photo-1545569341-9eb8b30979d9?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
        background-size: cover;
        background-position: center;
      "
    >
      <span class="mask bg-gradient-dark opacity-4"></span>
    </div>
    <div class="container">
      <div class="row mt-lg-n12 mt-md-n12 mt-n11 justify-content-center">
        <div class="col-xl-4 col-lg-5 col-md-7 mx-auto">
          <div class="card mt-8">
            <div class="card-header p-0 position-relative mt-n4 mx-3 z-index-2">
              <div
                class="bg-gradient-success shadow-success border-radius-lg py-3 pe-1 text-center py-4"
              >
                <h4 class="font-weight-bolder text-white mt-1">
                  Join us today
                </h4>
                <p class="mb-1 text-white text-sm">
                  Enter your email and password to register
                </p>
              </div>
            </div>
            <div class="card-body pb-3">
              <form role="form">
                <div class="mb-3">
                  <vmd-input label="Name" />
                </div>
                <div class="mb-3">
                  <vmd-input type="email" label="Email" />
                </div>
                <div class="mb-3">
                  <vmd-input type="password" label="Password" />
                </div>
                <vmd-checkbox
                  id="flexCheckDefault"
                  class="font-weight-light"
                  checked
                >
                  I agree the
                  <a
                    href="../../../pages/privacy.html"
                    class="text-dark font-weight-bolder"
                    >Terms and Conditions</a
                  >
                </vmd-checkbox>
                <div class="text-center">
                  <vmd-button
                    color="success"
                    variant="gradient"
                    fullWidth
                    class="mt-4 mb-0"
                    >Sign up</vmd-button
                  >
                </div>
              </form>
            </div>
            <div class="card-footer text-center pt-0 px-sm-4 px-1">
              <p class="mb-4 mx-auto">
                Already have an account?
                <a
                  href="../../../pages/sign-in/sign-in-cover.html"
                  class="text-success text-gradient font-weight-bold"
                  >Sign in</a
                >
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
  <app-footer />
</template>

<script>
import Navbar from "@/examples/PageLayout/Navbar.vue";
import AppFooter from "@/examples/PageLayout/Footer.vue";
import VmdInput from "@/components/VmdInput.vue";
import VmdCheckbox from "@/components/VmdCheckbox.vue";
import VmdButton from "@/components/VmdButton.vue";
const body = document.getElementsByTagName("body")[0];

export default {
  name: "signin-cover",
  components: {
    Navbar,
    AppFooter,
    VmdInput,
    VmdCheckbox,
    VmdButton,
  },
  created() {
    this.$store.state.hideConfigButton = true;
    this.$store.state.showNavbar = false;
    this.$store.state.showSidenav = false;
    this.$store.state.showFooter = false;
    body.classList.remove("bg-gray-100");
  },
  beforeUnmount() {
    this.$store.state.hideConfigButton = false;
    this.$store.state.showNavbar = true;
    this.$store.state.showSidenav = true;
    this.$store.state.showFooter = true;
    body.classList.add("bg-gray-100");
  },
};
</script>
