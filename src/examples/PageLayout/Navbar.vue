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
        >Material Dashboard 2 PRO</a
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
              id="dropdownMenuPages"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Pages
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
              class="p-3 mt-0 dropdown-menu dropdown-menu-animation dropdown-xl border-radius-xl mt-lg-3"
              aria-labelledby="dropdownMenuPages"
            >
              <div class="row d-none d-lg-block">
                <div class="px-4 py-2 col-12">
                  <div class="row">
                    <div class="col-4 position-relative">
                      <div
                        class="px-0 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                      >
                        <i class="material-icons opacity-6 me-2 text-md"
                          >dashboard</i
                        >
                        Dashboards
                      </div>
                      <router-link
                        :to="{ name: 'Default' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Analytics</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Sales' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Sales</span>
                      </router-link>
                      <div
                        class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                      >
                        <i
                          class="material-icons text-dark opacity-6 me-2 text-md"
                          >people</i
                        >
                        Users
                      </div>
                      <router-link
                        :to="{ name: 'New User' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">New User</span>
                      </router-link>
                      <hr class="vertical dark" />
                    </div>
                    <div class="col-4 position-relative">
                      <div
                        class="px-0 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                      >
                        <i
                          class="material-icons text-dark opacity-6 me-2 text-md"
                          >badge</i
                        >
                        Profile
                      </div>
                      <router-link
                        :to="{ name: 'All Projects' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Projects</span>
                      </router-link>
                      <div
                        class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                      >
                        <i
                          class="material-icons text-dark opacity-6 me-2 text-md"
                          >precision_manufacturing</i
                        >
                        Projects
                      </div>
                      <router-link
                        :to="{ name: 'General' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">General</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Timeline' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Timeline</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'New Project' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">New Project</span>
                      </router-link>
                      <hr class="vertical dark" />
                    </div>
                    <div class="col-4">
                      <div
                        class="px-0 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                      >
                        <i
                          class="material-icons text-dark opacity-6 me-2 text-md"
                          >account_balance</i
                        >
                        Account
                      </div>
                      <router-link
                        :to="{ name: 'Settings' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Settings</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Billing' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Billing</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Invoice' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Invoice</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Security' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Security</span>
                      </router-link>
                      <div
                        class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                      >
                        <i
                          class="material-icons text-dark opacity-6 me-2 text-md"
                          >queue_play_next</i
                        >
                        Extra
                      </div>
                      <router-link
                        :to="{ name: 'Pricing Page' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Pricing Page</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'RTL' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">RTL Page</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Widgets' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Widgets</span>
                      </router-link>
                    </div>
                  </div>
                </div>
              </div>
              <!-- responsive -->
              <div class="d-lg-none">
                <div
                  class="px-0 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons text-dark opacity-6 me-2 text-md"
                    >dashboard</i
                  >
                  Dashboards
                </div>
                <router-link
                  :to="{ name: 'Default' }"
                  class="dropdown-item border-radius-md"
                  >Default</router-link
                >
                <router-link
                  :to="{ name: 'Sales' }"
                  class="dropdown-item border-radius-md"
                  >Sales</router-link
                >
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons text-dark opacity-6 me-2 text-md"
                    >people</i
                  >
                  Users
                </div>
                <router-link to="#" class="dropdown-item border-radius-md"
                  >New user</router-link
                >
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons text-dark opacity-6 me-2 text-md"
                    >badge</i
                  >
                  Profile
                </div>
                <router-link to="#" class="dropdown-item border-radius-md"
                  >Projects</router-link
                >
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons text-dark opacity-6 me-2 text-md"
                    >precision_manufacturing</i
                  >
                  Projects
                </div>
                <router-link
                  :to="{ name: 'General' }"
                  class="dropdown-item border-radius-md"
                  >General</router-link
                >
                <router-link
                  :to="{ name: 'Timeline' }"
                  class="dropdown-item border-radius-md"
                  >Timeline</router-link
                >
                <router-link
                  :to="{ name: 'New Project' }"
                  class="dropdown-item border-radius-md"
                  >New Project</router-link
                >
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons text-dark opacity-6 me-2 text-md"
                    >account_balance</i
                  >
                  Account
                </div>
                <router-link
                  :to="{ name: 'Settings' }"
                  class="dropdown-item border-radius-md"
                  >Settings</router-link
                >
                <router-link
                  :to="{ name: 'Billing' }"
                  class="dropdown-item border-radius-md"
                  >Billing</router-link
                >
                <router-link
                  :to="{ name: 'Invoice' }"
                  class="dropdown-item border-radius-md"
                  >Invoice</router-link
                >
                <router-link
                  :to="{ name: 'Security' }"
                  class="dropdown-item border-radius-md"
                  >Security</router-link
                >
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons text-dark opacity-6 me-2 text-md"
                    >queue_play_next</i
                  >
                  Extra
                </div>
                <router-link
                  :to="{ name: 'Pricing Page' }"
                  class="dropdown-item border-radius-md"
                  >Pricing Page</router-link
                >
                <router-link
                  :to="{ name: 'RTL' }"
                  class="dropdown-item border-radius-md"
                  >RTL Page</router-link
                >
                <router-link
                  :to="{ name: 'Widgets' }"
                  class="dropdown-item border-radius-md"
                  >Widgets</router-link
                >
              </div>
            </div>
          </li>
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
                      <div
                        class="px-2 py-3 mt-0 dropdown-menu"
                        aria-labelledby="dropdownSignIn"
                      >
                        <router-link
                          class="mb-1 dropdown-item ps-3 border-radius-md"
                          :to="{ name: 'Signin Basic' }"
                        >
                          <span>Basic</span>
                        </router-link>
                        <router-link
                          class="mb-1 dropdown-item ps-3 border-radius-md"
                          :to="{ name: 'Signin Cover' }"
                        >
                          <span>Cover</span>
                        </router-link>
                        <router-link
                          class="mb-1 dropdown-item ps-3 border-radius-md"
                          :to="{ name: 'Signin Illustration' }"
                        >
                          <span>Illustration</span>
                        </router-link>
                      </div>
                    </li>
                    <li
                      class="nav-item dropdown dropdown-hover dropdown-subitem list-group-item border-0 p-0"
                    >
                      <a
                        class="mb-1 dropdown-item border-radius-md ps-3 d-flex align-items-center"
                        id="dropdownSignUp"
                      >
                        <i class="material-icons opacity-6 me-2 text-md"
                          >assignment</i
                        >

                        <span>Sign Up</span>
                        <img
                          src="@/assets/img/down-arrow.svg"
                          alt="down-arrow"
                          class="arrow ms-auto"
                        />
                      </a>
                      <div
                        class="px-2 py-3 mt-0 dropdown-menu"
                        aria-labelledby="dropdownSignUp"
                      >
                        <router-link
                          class="mb-1 dropdown-item ps-3 border-radius-md"
                          :to="{ name: 'Signup Cover' }"
                        >
                          <span>Cover</span>
                        </router-link>
                      </div>
                    </li>
                    <li
                      class="nav-item dropdown dropdown-hover dropdown-subitem list-group-item border-0 p-0"
                    >
                      <a
                        class="mb-1 dropdown-item border-radius-md ps-3 d-flex align-items-center"
                        id="dropdownSignUp"
                      >
                        <i class="material-icons opacity-6 me-2 text-md"
                          >restart_alt</i
                        >

                        <span>Reset Password</span>
                        <img
                          src="@/assets/img/down-arrow.svg"
                          alt="down-arrow"
                          class="arrow ms-auto"
                        />
                      </a>
                      <div
                        class="px-2 py-3 mt-0 dropdown-menu"
                        aria-labelledby="dropdownPasswordReset"
                      >
                        <router-link
                          class="mb-1 dropdown-item ps-3 border-radius-md"
                          :to="{ name: 'Reset Cover' }"
                        >
                          <span>Cover</span>
                        </router-link>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="row d-lg-none">
                <div class="col-12 d-flex justify-content-center flex-column">
                  <h6
                    class="px-0 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                  >
                    <i class="material-icons opacity-6 me-2 text-md">login</i>
                    Sign In
                  </h6>
                  <router-link
                    :to="{ name: 'Signin Basic' }"
                    class="dropdown-item border-radius-md"
                    >Basic</router-link
                  >
                  <router-link
                    :to="{ name: 'Signin Cover' }"
                    class="dropdown-item border-radius-md"
                    >Cover</router-link
                  >
                  <router-link
                    :to="{ name: 'Signin Illustration' }"
                    class="dropdown-item border-radius-md"
                    >Illustration</router-link
                  >
                  <h6
                    class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                  >
                    <i class="material-icons opacity-6 me-2 text-md"
                      >assignment</i
                    >
                    Sign Up
                  </h6>
                  <router-link
                    :to="{ name: 'Signup Cover' }"
                    class="dropdown-item border-radius-md"
                    >Cover</router-link
                  >
                  <h6
                    class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                  >
                    <i class="material-icons opacity-6 me-2 text-md"
                      >restart_alt</i
                    >
                    Reset Password
                  </h6>
                  <router-link
                    :to="{ name: 'Reset Cover' }"
                    class="dropdown-item border-radius-md"
                    >Cover</router-link
                  >
                </div>
              </div>
            </div>
          </li>
          <li class="mx-2 nav-item dropdown dropdown-hover">
            <a
              role="button"
              class="cursor-pointer nav-link ps-2 d-flex justify-content-between align-items-center"
              :class="[darkModes]"
              id="dropdownMenuBlocks"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Applications
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
              class="p-3 mt-0 dropdown-menu dropdown-menu-animation dropdown-md dropdown-md-responsive border-radius-lg mt-lg-3"
              aria-labelledby="dropdownMenuBlocks"
            >
              <div class="d-none d-lg-block">
                <ul class="list-group">
                  <li
                    class="p-0 border-0 nav-item dropdown dropdown-hover dropdown-subitem list-group-item"
                  >
                    <router-link
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      :to="{ name: 'Kanban' }"
                    >
                      <div class="d-flex align-items-center text-dark">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >widgets</i
                        >
                        Kanban
                      </div>
                    </router-link>
                  </li>
                  <li
                    class="p-0 border-0 nav-item dropdown dropdown-hover dropdown-subitem list-group-item"
                  >
                    <router-link
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      :to="{ name: 'Wizard' }"
                    >
                      <div class="d-flex align-items-center text-dark">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >import_contacts</i
                        >
                        Wizard
                      </div>
                    </router-link>
                  </li>
                  <li
                    class="p-0 border-0 nav-item dropdown dropdown-hover dropdown-subitem list-group-item"
                  >
                    <router-link
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      :to="{ name: 'Data Tables' }"
                    >
                      <div class="d-flex align-items-center text-dark">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >backup_table</i
                        >
                        DataTables
                      </div>
                    </router-link>
                  </li>
                  <li
                    class="p-0 border-0 nav-item dropdown dropdown-hover dropdown-subitem list-group-item"
                  >
                    <router-link
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      :to="{ name: 'Calendar' }"
                    >
                      <div class="d-flex align-items-center text-dark">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >event</i
                        >
                        Calendar
                      </div>
                    </router-link>
                  </li>
                </ul>
              </div>
              <!-- responsive -->
              <div class="row d-lg-none">
                <div class="col-md-12">
                  <router-link
                    class="py-2 ps-3 border-radius-md"
                    :to="{ name: 'Kanban' }"
                  >
                    <div class="d-flex align-items-center text-dark">
                      <i class="material-icons opacity-6 me-2 text-md"
                        >widgets</i
                      >
                      Kanban
                    </div>
                  </router-link>
                  <router-link
                    class="py-2 ps-3 border-radius-md"
                    :to="{ name: 'Wizard' }"
                  >
                    <div class="d-flex align-items-center text-dark">
                      <i class="material-icons opacity-6 me-2 text-md"
                        >import_contacts</i
                      >
                      Wizard
                    </div>
                  </router-link>
                  <router-link
                    class="py-2 ps-3 border-radius-md"
                    :to="{ name: 'Data Tables' }"
                  >
                    <div class="d-flex align-items-center text-dark">
                      <i class="material-icons opacity-6 me-2 text-md"
                        >backup_table</i
                      >
                      DataTables
                    </div>
                  </router-link>
                  <router-link
                    class="py-2 ps-3 border-radius-md"
                    :to="{ name: 'Calendar' }"
                  >
                    <div class="d-flex align-items-center text-dark">
                      <i class="material-icons opacity-6 me-2 text-md">event</i>
                      Calendar
                    </div>
                  </router-link>
                </div>
              </div>
            </div>
          </li>
          <li class="mx-2 nav-item dropdown dropdown-hover">
            <a
              role="button"
              class="cursor-pointer nav-link ps-2 d-flex justify-content-between align-items-center"
              :class="[darkModes]"
              id="dropdownMenuEcommerce"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Ecommerce
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
                :class="darkMode ? 'd-lg-block' : ' d-lg-none'"
              />
            </a>
            <div
              class="p-3 mt-0 dropdown-menu dropdown-menu-animation dropdown-lg border-radius-xl mt-lg-3"
              aria-labelledby="dropdownMenuEcommerce"
            >
              <div class="row d-none d-lg-block">
                <div class="px-4 py-2 col-12">
                  <div class="row">
                    <div class="col-6 position-relative">
                      <div
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center px-0"
                      >
                        <i class="material-icons opacity-6 me-2 text-md"
                          >shopping_cart</i
                        >
                        Orders
                      </div>
                      <router-link
                        :to="{ name: 'Order List' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Order List</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Order Details' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Order Details</span>
                      </router-link>
                      <hr class="vertical dark" />
                    </div>
                    <div class="col-6 position-relative">
                      <div
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center px-0"
                      >
                        <i class="material-icons opacity-6 me-2 text-md"
                          >memory</i
                        >
                        Products
                      </div>
                      <router-link
                        :to="{ name: 'New Product' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">New Product</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Edit Product' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Edit Product</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Product Page' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Product Page</span>
                      </router-link>
                      <router-link
                        :to="{ name: 'Products List' }"
                        class="dropdown-item border-radius-md"
                      >
                        <span class="ps-3">Products List</span>
                      </router-link>
                    </div>
                  </div>
                </div>
              </div>
              <!-- responsive -->
              <div class="d-lg-none">
                <div
                  class="px-0 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons opacity-6 me-2 text-md"
                    >shopping_cart</i
                  >
                  Orders
                </div>
                <router-link
                  :to="{ name: 'Order List' }"
                  class="dropdown-item border-radius-md"
                  >Order List</router-link
                >
                <router-link
                  :to="{ name: 'Order Details' }"
                  class="dropdown-item border-radius-md"
                  >Order Details</router-link
                >
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons opacity-6 me-2 text-md">store</i>
                  General
                </div>
                <div
                  class="px-0 mt-3 dropdown-header text-dark font-weight-bolder d-flex align-items-center"
                >
                  <i class="material-icons opacity-6 me-2 text-md">memory</i>
                  Products
                </div>
                <router-link
                  :to="{ name: 'New Product' }"
                  class="dropdown-item border-radius-md"
                  >New Product</router-link
                >
                <router-link
                  :to="{ name: 'Edit Product' }"
                  class="dropdown-item border-radius-md"
                  >Edit Product</router-link
                >
                <router-link
                  :to="{ name: 'Product Page' }"
                  class="dropdown-item border-radius-md"
                  >Product Page</router-link
                >
                <router-link
                  :to="{ name: 'Products List' }"
                  class="dropdown-item border-radius-md"
                  >Products List</router-link
                >
              </div>
            </div>
          </li>
          <li class="mx-2 nav-item dropdown dropdown-hover">
            <a
              role="button"
              class="cursor-pointer nav-link ps-2 d-flex justify-content-between align-items-center"
              :class="[darkModes]"
              id="dropdownMenuDocs"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Docs
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
              class="p-3 mt-0 dropdown-menu dropdown-menu-animation dropdown-lg mt-lg-3 border-radius-lg"
              aria-labelledby="dropdownMenuDocs"
            >
              <div class="d-none d-lg-block">
                <ul class="list-group">
                  <li class="p-0 border-0 nav-item list-group-item">
                    <a
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      href="https://www.creative-tim.com/learning-lab/vue/overview/material-dashboard"
                    >
                      <div class="d-flex align-items-center">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >article</i
                        >
                        <h6
                          class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0 mb-0"
                        >
                          Getting Started
                        </h6>
                      </div>
                      <span class="text-sm opacity-8 ps-4"
                        >All about overview, quick start, license and
                        contents</span
                      >
                    </a>
                  </li>
                  <li class="p-0 border-0 nav-item list-group-item">
                    <a
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/colors/soft-ui-dashboard"
                    >
                      <div class="d-flex align-items-center">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >grading</i
                        >
                        <h6
                          class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0 mb-0"
                        >
                          Foundation
                        </h6>
                      </div>
                      <span class="text-sm opacity-8 ps-4"
                        >See our colors, icons and typography</span
                      >
                    </a>
                  </li>
                  <li class="p-0 border-0 nav-item list-group-item">
                    <a
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/alerts/soft-ui-dashboard"
                    >
                      <div class="d-flex align-items-center">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >apps</i
                        >
                        <h6
                          class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0 mb-0"
                        >
                          Components
                        </h6>
                      </div>
                      <span class="text-sm opacity-8 ps-4"
                        >Explore our collection of fully designed
                        components</span
                      >
                    </a>
                  </li>
                  <li class="p-0 border-0 nav-item list-group-item">
                    <a
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/datepicker/soft-ui-dashboard"
                    >
                      <div class="d-flex align-items-center">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >extension</i
                        >
                        <h6
                          class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0 mb-0"
                        >
                          Plugins
                        </h6>
                      </div>
                      <span class="text-sm opacity-8 ps-4"
                        >Check how you can integrate our plugins</span
                      >
                    </a>
                  </li>
                  <li class="p-0 border-0 nav-item list-group-item">
                    <a
                      class="py-2 dropdown-item ps-3 border-radius-md"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/utilities/soft-ui-dashboard"
                    >
                      <div class="d-flex align-items-center">
                        <i class="material-icons opacity-6 me-2 text-md"
                          >swipe</i
                        >
                        <h6
                          class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0 mb-0"
                        >
                          Utility Classes
                        </h6>
                      </div>
                      <span class="text-sm opacity-8 ps-4"
                        >For those who want flexibility, use our utility
                        classes</span
                      >
                    </a>
                  </li>
                </ul>
              </div>
              <div class="row d-lg-none">
                <div class="col-md-12 g-0">
                  <a
                    class="py-2 dropdown-item ps-3 border-radius-md"
                    href="../../pages/about-us.html"
                  >
                    <div class="d-flex align-items-center">
                      <i class="material-icons opacity-6 me-2 text-md"
                        >article</i
                      >
                      <h6
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0"
                      >
                        Getting Started
                      </h6>
                    </div>
                    <span class="text-sm ps-4"
                      >All about overview, quick start, license and
                      contents</span
                    >
                  </a>
                  <a
                    class="py-2 dropdown-item ps-3 border-radius-md"
                    href="../../pages/about-us.html"
                  >
                    <div class="d-flex align-items-center">
                      <i class="material-icons opacity-6 me-2 text-md"
                        >grading</i
                      >
                      <h6
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0"
                      >
                        Foundation
                      </h6>
                    </div>
                    <span class="text-sm ps-4"
                      >See our colors, icons and typography</span
                    >
                  </a>
                  <a
                    class="py-2 dropdown-item ps-3 border-radius-md"
                    href="../../pages/about-us.html"
                  >
                    <div class="d-flex align-items-center">
                      <i class="material-icons opacity-6 me-2 text-md">apps</i>
                      <h6
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0"
                      >
                        Components
                      </h6>
                    </div>
                    <span class="text-sm ps-4"
                      >Explore our collection of fully designed components</span
                    >
                  </a>
                  <a
                    class="py-2 dropdown-item ps-3 border-radius-md"
                    href="../../pages/about-us.html"
                  >
                    <div class="d-flex align-items-center">
                      <i class="material-icons opacity-6 me-2 text-md"
                        >extension</i
                      >
                      <h6
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0"
                      >
                        Plugins
                      </h6>
                      <span class="text-sm ps-4"
                        >Check how you can integrate our plugins</span
                      >
                    </div>
                  </a>
                  <a
                    class="py-2 dropdown-item ps-3 border-radius-md"
                    href="../../pages/about-us.html"
                  >
                    <div class="d-flex align-items-center">
                      <i class="material-icons opacity-6 me-2 text-md">swipe</i>
                      <h6
                        class="dropdown-header text-dark font-weight-bolder d-flex align-items-center p-0"
                      >
                        Utility Classes
                      </h6>
                      <span class="text-sm ps-4"
                        >All about overview, quick start, license and
                        contents</span
                      >
                    </div>
                  </a>
                </div>
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
