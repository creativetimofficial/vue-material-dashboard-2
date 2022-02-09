<template>
  <div class="bg-white">
    <div class="container top-0 position-sticky z-index-sticky">
      <div class="row">
        <div class="col-12">
          <navbar
            isBlur="blur my-3 py-2 mt-4 start-0 end-0 mx-4 shadow blur border-radius-lg"
            btnBackground="bg-gradient-success"
            v-bind:darkMode="true"
          />
        </div>
      </div>
    </div>
    <main class="mt-0 main-content">
      <section>
        <div class="page-header min-vh-100">
          <div class="container">
            <div class="row">
              <div
                class="col-6 d-lg-flex d-none h-100 my-auto pe-0 position-absolute top-0 start-0 text-center justify-content-center flex-column"
              >
                <div
                  class="position-relative h-100 m-3 px-7 border-radius-lg d-flex flex-column justify-content-center"
                  :style="{
                    backgroundImage:
                      'url(' +
                      require('@/assets/img/illustrations/illustration-signin.jpg') +
                      ')',
                  }"
                ></div>
              </div>
              <div
                class="col-xl-4 col-lg-5 col-md-7 d-flex flex-column ms-auto me-auto ms-lg-auto me-lg-5"
              >
                <div class="card card-plain">
                  <div class="pb-0 card-header text-center bg-transparent mb-4">
                    <h4 class="font-weight-bolder">Sign In</h4>
                    <p class="mb-0">Enter your email and password to sign in</p>
                  </div>
                  <div class="card-body">
                    <form role="form">
                      <div class="mb-3">
                        <vmd-input
                          type="email"
                          label="Email"
                          name="email"
                          size="lg"
                        />
                      </div>
                      <div class="mb-3">
                        <vmd-input
                          type="password"
                          label="Password"
                          name="password"
                          size="lg"
                        />
                      </div>
                      <vmd-switch id="rememberMe">Remember me</vmd-switch>

                      <div class="text-center">
                        <vmd-button
                          class="mt-4"
                          variant="gradient"
                          color="success"
                          fullWidth
                          size="lg"
                          >Sign in</vmd-button
                        >
                      </div>
                    </form>
                  </div>
                  <div class="px-1 pt-0 text-center card-footer px-lg-2">
                    <p class="mx-auto mb-4 text-sm">
                      Don't have an account?
                      <a
                        href="javascript:;"
                        class="text-success text-gradient font-weight-bold"
                        >Sign up</a
                      >
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
import Navbar from "@/examples/PageLayout/Navbar.vue";
import VmdInput from "@/components/VmdInput.vue";
import VmdSwitch from "@/components/VmdSwitch.vue";
import VmdButton from "@/components/VmdButton.vue";
const body = document.getElementsByTagName("body")[0];

export default {
  name: "signin-illustration",
  components: {
    Navbar,
    VmdInput,
    VmdSwitch,
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
