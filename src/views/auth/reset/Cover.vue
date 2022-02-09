<template>
  <navbar btnBackground="bg-gradient-success" />

  <main class="mt-0 main-content">
    <div
      class="page-header align-items-start min-vh-50 m-3 border-radius-lg"
      style="
        background-image: url('https://images.unsplash.com/photo-1497996541515-6549b145cd90?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1650&q=80');
      "
    >
      <span class="mask bg-gradient-dark opacity-6"></span>
    </div>
    <section>
      <div class="container mb-4">
        <div class="row mt-lg-n12 mt-md-n12 mt-n12 justify-content-center">
          <div class="col-xl-4 col-lg-5 col-md-7 mx-auto">
            <div class="card mt-8">
              <div
                class="card-header p-0 position-relative mt-n4 mx-3 z-index-2"
              >
                <div
                  class="bg-gradient-warning shadow-warning border-radius-lg py-3 pe-1 text-center py-4"
                >
                  <h3 class="font-weight-bolder text-white">Reset Password</h3>
                  <p class="mb-0 text-sm text-white">
                    You will receive an e-mail in maximum 60 seconds
                  </p>
                </div>
              </div>
              <div class="py-4 card-body">
                <form role="form">
                  <div class="mb-3">
                    <vmd-input
                      type="email"
                      label="Email"
                      placeholder="john@email.com"
                      name="email"
                      variant="static"
                    />
                  </div>
                  <div class="text-center">
                    <vmd-button
                      class="mt-4"
                      variant="gradient"
                      color="warning"
                      fullWidth
                      >Reset</vmd-button
                    >
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
  <app-footer />
</template>

<script>
import Navbar from "@/examples/PageLayout/Navbar.vue";
import AppFooter from "@/examples/PageLayout/Footer.vue";
import VmdInput from "@/components/VmdInput.vue";
import VmdButton from "@/components/VmdButton.vue";
const body = document.getElementsByTagName("body")[0];

export default {
  name: "reset-cover",
  components: {
    Navbar,
    AppFooter,
    VmdInput,
    VmdButton,
  },
  beforeMount() {
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
