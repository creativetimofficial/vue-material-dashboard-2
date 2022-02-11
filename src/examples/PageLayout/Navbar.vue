<template>
  <!-- Navbar -->
  <nav
    class="top-0 navbar navbar-expand-lg position-absolute z-index-3"
    :class="isBlur ? isBlur : 'shadow-none my-3 navbar-transparent w-100 mt-4'"
  >
    <div class="container" :class="isBlur && 'px-1'">
      <a
        class="navbar-brand font-weight-bolder ms-lg-0 ms-3"
        :class="darkMode ? 'text-black' : 'text-white'"
        href="/"
        >Material Dashboard 2</a
      >
      <button
        class="shadow-none navbar-toggler ms-2"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navigation"
        aria-controls="navigation"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="mt-2 navbar-toggler-icon">
          <span class="navbar-toggler-bar bar1"></span>
          <span class="navbar-toggler-bar bar2"></span>
          <span class="navbar-toggler-bar bar3"></span>
        </span>
      </button>
      <div
        class="pt-3 pb-2 collapse navbar-collapse w-100 py-lg-0"
        id="navigation"
      >
        <ul class="mx-auto navbar-nav navbar-nav-hover">
      
          <li class="mx-2 nav-item dropdown dropdown-hover">
            <a
              role="button"
              class="cursor-pointer nav-link ps-2 d-flex justify-content-between align-items-center"
              :class="[darkModes]"
              id="dropdownMenuAccount"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Authentication
              <img
                :src="downArrWhite"
                alt="down-arrow"
                class="arrow ms-1"
                :class="darkMode ? 'd-none' : 'd-lg-block d-none'"
              />
              <img
                :src="downArrBlack"
                alt="down-arrow"
                class="arrow ms-1 d-block"
                :class="darkMode ? 'd-lg-block' : 'd-lg-none'"
              />
            </a>
            <div
              class="dropdown-menu dropdown-menu-animation dropdown-md border-radius-xl p-3 mt-0 mt-lg-3"
              aria-labelledby="dropdownMenuAccount"
            >
              <div class="d-none d-lg-flex">
                <div
                  class="col-12 ps-0 d-flex justify-content-center flex-column"
                >
                  <ul class="list-group">
                    <li
                      class="nav-item dropdown dropdown-hover dropdown-subitem list-group-item border-0 p-0"
                    >
                      <a
                        class="mb-1 dropdown-item border-radius-md ps-3 d-flex align-items-center"
                        id="dropdownSignUp"
                      >
                        <i class="material-icons opacity-6 me-2 text-md"
                          >login</i
                        >

                        <span>Sign In</span>
                        <img
                          src="@/assets/img/down-arrow.svg"
                          alt="down-arrow"
                          class="arrow ms-auto"
                        />
                      </a>
                    
                    </li>
                    
                  
                  </ul>
                </div>
              </div>
              <div class="row d-lg-none">
                
              </div>
            </div>
          </li>
         
        </ul>
        <ul class="navbar-nav d-lg-block d-none">
          <li class="nav-item">
            <a
              href="javascript:;"
              class="mb-0 btn btn-sm me-1"
              :class="btnBackground ? btnBackground : 'bg-white'"
              onclick="smoothToPricing('pricing-soft-ui')"
              >Buy Now</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <!-- End Navbar -->
</template>

<script>
import downArrWhite from "@/assets/img/down-arrow-white.svg";
import downArrBlack from "@/assets/img/down-arrow-dark.svg";

export default {
  name: "navbar",
  data() {
    return {
      downArrWhite,
      downArrBlack,
    };
  },
  props: {
    btnBackground: String,
    isBlur: String,
    darkMode: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    darkModes() {
      return {
        "text-dark": this.darkMode,
      };
    },
  },
};
</script>
