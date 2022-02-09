<template>
  <div
    class="w-auto h-auto collapse navbar-collapse max-height-vh-100 h-100"
    id="sidenav-collapse-main"
  >
    <ul class="navbar-nav">
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="brooklynAlice"
          navText="Brooklyn Alice"
          :class="getRoute() === 'brooklynAlice' ? 'active' : ''"
        >
          <template v-slot:icon>
            <img src="../../assets/img/team-3.jpg" class="avatar" />
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->
              <sidenav-item
                :to="{ name: 'Profile Overview' }"
                miniIcon="MP"
                text="My Profile"
              />
              <sidenav-item
                :to="{ name: 'Settings' }"
                miniIcon="S"
                text="Settings"
              />
              <sidenav-item
                :to="{ name: 'Signin Basic' }"
                miniIcon="L"
                text="Logout"
              />
            </ul>
          </template>
        </sidenav-collapse>
      </li>
      <hr class="horizontal light mt-2 mb-2" />
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="dashboardsExamples"
          navText="Dashboards"
          :class="getRoute() === 'dashboards' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">dashboard</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->
              <sidenav-item
                :to="{ name: 'Default' }"
                miniIcon="D"
                text="Analytics"
              />
              <sidenav-item :to="{ name: 'Sales' }" miniIcon="S" text="Sales" />
            </ul>
          </template>
        </sidenav-collapse>
      </li>
      <li class="mt-3 nav-item">
        <h6
          class="text-xs ps-4 text-uppercase font-weight-bolder text-white"
          :class="this.$store.state.isRTL ? 'me-4' : 'ms-2'"
        >
          PAGES
        </h6>
      </li>
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="pagesExamples"
          navText="Pages"
          :class="getRoute() === 'pages' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">image</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->
              <sidenav-collapse-item
                refer="profileExample"
                miniIcon="P"
                text="Profile"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Profile Overview' }"
                    miniIcon="P"
                    text="Profile Overview"
                  />
                  <sidenav-item
                    :to="{ name: 'All Projects' }"
                    miniIcon="A"
                    text="All Projects"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="usersExample"
                miniIcon="U"
                text="Users"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'New User' }"
                    miniIcon="N"
                    text="New User"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="accountExample"
                miniIcon="A"
                text="Account"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Settings' }"
                    miniIcon="S"
                    text="Settings"
                  />
                  <sidenav-item
                    :to="{ name: 'Billing' }"
                    miniIcon="B"
                    text="Billing"
                  />
                  <sidenav-item
                    :to="{ name: 'Invoice' }"
                    miniIcon="I"
                    text="Invoice"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="projectsExample"
                miniIcon="P"
                text="Projects"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Timeline' }"
                    miniIcon="T"
                    text="Timeline"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-item
                :to="{ name: 'Pricing Page' }"
                miniIcon="P"
                text="Pricing Page"
              />
              <sidenav-item :to="{ name: 'RTL' }" miniIcon="R" text="RTL" />
              <sidenav-item
                :to="{ name: 'Widgets' }"
                miniIcon="W"
                text="Widgets"
              />
              <sidenav-item
                :to="{ name: 'Charts' }"
                miniIcon="C"
                text="Charts"
              />
              <sidenav-item
                :to="{ name: 'Notifications' }"
                miniIcon="N"
                text="Notifications"
              />
            </ul>
          </template>
        </sidenav-collapse>
      </li>

      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="applicationsExamples"
          navText="Applications"
          :class="getRoute() === 'applications' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">apps</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->

              <sidenav-item
                :to="{ name: 'Kanban' }"
                miniIcon="K"
                text="Kanban"
              />
              <sidenav-item
                :to="{ name: 'Wizard' }"
                miniIcon="W"
                text="Wizard"
              />
              <sidenav-item
                :to="{ name: 'Data Tables' }"
                miniIcon="D"
                text="Data Tables"
              />
              <sidenav-item
                :to="{ name: 'Calendar' }"
                miniIcon="C"
                text="Calendar"
              />
            </ul>
          </template>
        </sidenav-collapse>
      </li>

      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="ecommerceExamples"
          navText="Ecommerce"
          :class="getRoute() === 'ecommerce' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">shopping_basket</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->

              <sidenav-collapse-item
                refer="productsExample"
                miniIcon="P"
                text="Products"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'New Product' }"
                    miniIcon="N"
                    text="New Product"
                  />
                  <sidenav-item
                    :to="{ name: 'Edit Product' }"
                    miniIcon="E"
                    text="Edit Product"
                  />
                  <sidenav-item
                    :to="{ name: 'Product Page' }"
                    miniIcon="P"
                    text="Product page"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="ordersExample"
                miniIcon="O"
                text="Orders"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Order List' }"
                    miniIcon="O"
                    text="Order List"
                  />
                  <sidenav-item
                    :to="{ name: 'Order Details' }"
                    miniIcon="O"
                    text="Order Details"
                  />
                </template>
              </sidenav-collapse-item>
            </ul>
          </template>
        </sidenav-collapse>
      </li>

      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="authExamples"
          navText="Authentication"
          :class="getRoute() === 'authentication' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">content_paste</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->
              <sidenav-collapse-item
                refer="signinExample"
                miniIcon="S"
                text="Sign In"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Signin Basic' }"
                    miniIcon="B"
                    text="Basic"
                  />
                  <sidenav-item
                    :to="{ name: 'Signin Cover' }"
                    miniIcon="C"
                    text="Cover"
                  />
                  <sidenav-item
                    :to="{ name: 'Signin Illustration' }"
                    miniIcon="I"
                    text="Illustration"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="signupExample"
                miniIcon="S"
                text="Sign Up"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Signup Cover' }"
                    miniIcon="C"
                    text="Cover"
                  />
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="resetExample"
                miniIcon="R"
                text="Reset Password"
              >
                <template v-slot:nav-child-item>
                  <sidenav-item
                    :to="{ name: 'Reset Cover' }"
                    miniIcon="C"
                    text="Cover"
                  />
                </template>
              </sidenav-collapse-item>
            </ul>
          </template>
        </sidenav-collapse>
      </li>
      <li class="mt-3 nav-item">
        <hr class="horizontal light mt-0" />
        <h6
          class="text-xs ps-4 ms-2 text-uppercase font-weight-bolder text-white"
          :class="this.$store.state.isRTL ? 'me-4' : 'ms-2'"
        >
          DOCS
        </h6>
      </li>
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="basicExamples"
          navText="Basic"
          icon="dashboard"
          :class="getRoute() === 'basic' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">upcoming</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->
              <sidenav-collapse-item
                refer="gettingStartedExample"
                miniIcon="G"
                text="Getting Started"
              >
                <template v-slot:nav-child-item>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/quick-start/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">Q</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Quick Start</span
                      >
                    </a>
                  </li>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/license/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">L</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >License</span
                      >
                    </a>
                  </li>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/overview/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">C</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Contents</span
                      >
                    </a>
                  </li>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/build-tools/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">B</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Build Tools</span
                      >
                    </a>
                  </li>
                </template>
              </sidenav-collapse-item>

              <sidenav-collapse-item
                refer="foundationExample"
                miniIcon="F"
                text="Foundation"
              >
                <template v-slot:nav-child-item>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/colors/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">C</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Colors</span
                      >
                    </a>
                  </li>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/grid/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">G</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Grid</span
                      >
                    </a>
                  </li>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/typography/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">T</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Typography</span
                      >
                    </a>
                  </li>
                  <li
                    class="nav-item"
                    :class="getRoute() === 'dashboards' ? 'active' : ''"
                  >
                    <a
                      class="nav-link"
                      href="https://www.creative-tim.com/learning-lab/bootstrap/icons/soft-ui-dashboard"
                      target="_blank"
                    >
                      <span class="text-xs sidenav-mini-icon">I</span>
                      <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                        >Icons</span
                      >
                    </a>
                  </li>
                </template>
              </sidenav-collapse-item>
            </ul>
          </template>
        </sidenav-collapse>
      </li>
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          collapseRef="componentsExamples"
          navText="Components"
          :class="getRoute() === 'components' ? 'active' : ''"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">view_in_ar</i>
          </template>
          <template v-slot:list>
            <ul class="nav pe-0">
              <!-- nav links -->
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/alerts/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">A</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Alerts</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/badge/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">B</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Badge</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/buttons/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">B</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Buttons</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/cards/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">C</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Card</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/carousel/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">C</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Carousel</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/collapse/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">C</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Collapse</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/dropdowns/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">D</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Dropdowns</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/forms/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">F</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Forms</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/modal/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">M</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Modal</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/navs/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">N</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Navs</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/navbar/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">N</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Navbar</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/pagination/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">P</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Pagination</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/popovers/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">P</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Popovers</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/progress/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">P</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Progress</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/spinners/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">S</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Spinners</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/tables/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">T</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Tables</span
                  >
                </a>
              </li>
              <li
                class="nav-item"
                :class="getRoute() === 'dashboards' ? 'active' : ''"
              >
                <a
                  class="nav-link"
                  href="https://www.creative-tim.com/learning-lab/bootstrap/tooltips/soft-ui-dashboard"
                  target="_blank"
                >
                  <span class="sidenav-mini-icon text-white">T</span>
                  <span class="sidenav-normal me-3 ms-3 ps-1 text-white"
                    >Tooltips</span
                  >
                </a>
              </li>
            </ul>
          </template>
        </sidenav-collapse>
      </li>
      <li class="nav-item" :class="getRoute() === 'dashboards' ? 'active' : ''">
        <sidenav-collapse
          navText="Changelog"
          v-bind:collapse="false"
          url="#"
          :aria-controls="''"
          collapseRef="https://github.com/creativetimofficial/ct-soft-ui-dashboard-pro/blob/main/CHANGELOG.md"
        >
          <template v-slot:icon>
            <i class="material-icons-round opacity-10">receipt_long</i>
          </template>
        </sidenav-collapse>
      </li>
    </ul>
  </div>
</template>
<script>
import SidenavItem from "./SidenavItem.vue";
import SidenavCollapse from "./SidenavCollapse.vue";
import SidenavCollapseItem from "./SidenavCollapseItem.vue";

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
    SidenavItem,
    SidenavCollapse,
    SidenavCollapseItem,
  },
  methods: {
    getRoute() {
      const routeArr = this.$route.path.split("/");
      return routeArr[1];
    },
  },
};
</script>
