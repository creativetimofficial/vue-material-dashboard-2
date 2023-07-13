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
                class="col-6 d-lg-flex d-none h-100 my-auto pe-0 ps-0 position-absolute top-0 start-0 text-center justify-content-center flex-column"
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
                  <div class="pb-0 card-header bg-transparent mb-4">
                    <h4 class="font-weight-bolder">Sign In</h4>
                    <p class="mb-0">
                      Enter your email and password to register
                    </p>
                  </div>
                  <div class="card-body">
                    <form role="form">
                      <div class="mb-3">
                        <material-input
                          type="text"
                          label="Name"
                          name="name"
                          size="lg"
                        />
                      </div>
                      <div class="mb-3">
                        <material-input
                          type="email"
                          label="Email"
                          name="email"
                          size="lg"
                        />
                      </div>
                      <div class="mb-3">
                        <material-input
                          type="password"
                          label="Password"
                          name="password"
                          size="lg"
                        />
                      </div>
                      <material-checkbox
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
                      </material-checkbox>
                      <div class="text-center">
                        <material-button
                          class="mt-4"
                          variant="gradient"
                          color="success"
                          fullWidth
                          size="lg"
                          >Sign Up</material-button
                        >
                      </div>
                    </form>
                  </div>
                  <div class="px-1 pt-0 text-center card-footer px-lg-2">
                    <p class="mx-auto mb-4 text-sm">
                      Don't have an account?
                      <router-link
                        :to="{ name: 'SignIn' }"
                        class="text-success text-gradient font-weight-bold"
                        >Sign In</router-link
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
import MaterialInput from "@/components/MaterialInput.vue";
import MaterialCheckbox from "@/components/MaterialCheckbox.vue";
import MaterialButton from "@/components/MaterialButton.vue";
const body = document.getElementsByTagName("body")[0];

export default {
  name: "sign-up",
  components: {
    Navbar,
    MaterialInput,
    MaterialCheckbox,
    MaterialButton,
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
