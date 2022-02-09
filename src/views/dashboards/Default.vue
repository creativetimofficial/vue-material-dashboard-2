<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-12 position-relative z-index-2">
        <div class="card mb-4">
          <div class="d-flex">
            <div
              class="icon icon-shape icon-lg bg-gradient-success shadow text-center border-radius-xl mt-n3 ms-4"
            >
              <i class="material-icons opacity-10" aria-hidden="true"
                >language</i
              >
            </div>
            <h6 class="mt-3 mb-2 ms-3">Sales by Country</h6>
          </div>
          <div class="card-body p-3">
            <div class="row">
              <div class="col-lg-6 col-md-7">
                <div class="table-responsive">
                  <table class="table align-items-center">
                    <tbody>
                      <tr v-for="(sale, index) in sales" :key="index">
                        <td class="w-30">
                          <div class="px-2 py-1 d-flex align-items-center">
                            <div>
                              <img :src="sale.flag" alt="Country flag" />
                            </div>
                            <div class="ms-4">
                              <p class="mb-0 text-xs font-weight-bold">
                                Country:
                              </p>
                              <h6 class="mb-0 text-sm font-weight-normal">
                                {{ sale.country }}
                              </h6>
                            </div>
                          </div>
                        </td>
                        <td>
                          <div class="text-center">
                            <p class="mb-0 text-xs font-weight-bold">Sales:</p>
                            <h6 class="mb-0 text-sm font-weight-normal">
                              {{ sale.sales }}
                            </h6>
                          </div>
                        </td>
                        <td>
                          <div class="text-center">
                            <p class="mb-0 text-xs font-weight-bold">Value:</p>
                            <h6 class="mb-0 text-sm font-weight-normal">
                              {{ sale.value }}
                            </h6>
                          </div>
                        </td>
                        <td class="text-sm align-middle">
                          <div class="text-center col">
                            <p class="mb-0 text-xs font-weight-bold">Bounce:</p>
                            <h6 class="mb-0 text-sm font-weight-normal">
                              {{ sale.bounce }}
                            </h6>
                          </div>
                        </td>
                      </tr>
                    </tbody>
                  </table>
                </div>
              </div>
              <div class="col-lg-6 col-md-5">
                <div id="map" class="mt-0 mt-lg-n4"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="row mb-4">
          <div class="col-lg-4 col-md-6 mt-4 mb-4">
            <chart-bars />
          </div>
          <div class="col-lg-4 col-md-6 mt-4 mb-4">
            <chart-line />
          </div>
          <div class="col-lg-4 mt-4 mb-3">
            <chart-line-tasks />
          </div>
        </div>
        <div class="row">
          <div class="col-lg-3 col-md-6 col-sm-6">
            <mini-cards
              title="Bookings"
              value="281"
              percentage="+55%"
              iconName="weekend"
              detail="than last week"
              iconClass="text-white"
              iconBackground="bg-gradient-dark"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-cards
              title="Today's Users"
              value="2,300"
              percentage="+3%"
              iconName="leaderboard"
              detail="than last month"
              iconClass="text-white"
              iconBackground="bg-gradient-primary"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-cards
              title="Revenue"
              value="34k"
              percentage="+1%"
              iconName="store"
              detail="than yesterday"
              iconClass="text-white"
              iconBackground="bg-gradient-success"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-cards
              title="Followers"
              value="+91"
              iconName="person_add"
              detail="Just updated"
              iconClass="text-white"
              iconBackground="bg-gradient-info"
            />
          </div>
        </div>
        <div class="row mt-5">
          <div class="col-lg-4 col-md-6">
            <booking-card
              :img="booking1"
              title="Cozy 5 Stars Apartment"
              description="The place is close to Barceloneta Beach and bus stop
            just 2 min by walk and near to 'Naviglio' where you can enjoy the
            main night life in Barcelona."
              price="$899/night"
              location="Barcelona, Spain"
            />
          </div>
          <div class="col-lg-4 col-md-6">
            <booking-card
              :img="booking2"
              title="Office Studio"
              description="The
            place is close to Metro Station and bus stop just 2 min by walk and
            near to 'Naviglio' where you can enjoy the night life in London,
            UK."
              price="$1.119/night"
              location="London, UK"
            />
          </div>
          <div class="col-lg-4 col-md-6">
            <booking-card
              :img="booking3"
              title="Beautiful Castle"
              description="The
            place is close to Metro Station and bus stop just 2 min by walk and
            near to 'Naviglio' where you can enjoy the night life in London,
            UK."
              price="$459/night"
              location="Milan, Italy"
            />
          </div>
        </div>
      </div>
    </div>

    <div class="row"></div>
  </div>
</template>
<script>
import "@/assets/js/world.js";

import ChartBars from "./components/ChartBars.vue";
import ChartLine from "./components/ChartLine.vue";
import ChartLineTasks from "./components/ChartLineTasks.vue";
import MiniCards from "./components/MiniCards.vue";
import BookingCard from "./components/BookingCard.vue";

import US from "../../assets/img/icons/flags/US.png";
import DE from "../../assets/img/icons/flags/DE.png";
import GB from "../../assets/img/icons/flags/GB.png";
import BR from "../../assets/img/icons/flags/BR.png";
import booking1 from "../../assets/img/products/product-1-min.jpg";
import booking2 from "../../assets/img/products/product-2-min.jpg";
import booking3 from "../../assets/img/products/product-3-min.jpg";

export default {
  name: "dashboard-default",
  data() {
    return {
      booking1,
      booking2,
      booking3,
      stats: {
        iconBackground: "bg-gradient-success",
        money: {
          title: "Today's Money",
          value: "$53,000",
          percentage: "+55%",
          iconClass: "ni ni-money-coins",
        },
        users: {
          title: "Today's Users",
          value: "2,300",
          percentage: "+3%",
          iconClass: "ni ni-world",
        },
        clients: {
          title: "New Clients",
          value: "+3,462",
          percentage: "-2%",
          iconClass: "ni ni-paper-diploma",
          percentageColor: "text-danger",
        },
        sales: {
          title: "Sales",
          value: "$103,430",
          percentage: "+5%",
          iconClass: "ni ni-cart",
        },
      },
      sales: {
        us: {
          country: "United States",
          sales: 2500,
          value: "$230,900",
          bounce: "29.9%",
          flag: US,
        },
        germany: {
          country: "Germany",
          sales: "3.900",
          value: "$440,000",
          bounce: "40.22%",
          flag: DE,
        },
        britain: {
          country: "Great Britain",
          sales: "1.400",
          value: "$190,700",
          bounce: "23.44%",
          flag: GB,
        },
        brasil: {
          country: "Brasil",
          sales: "562",
          value: "$143,960",
          bounce: "32.14%",
          flag: BR,
        },
      },
    };
  },
  components: { ChartBars, ChartLine, ChartLineTasks, MiniCards, BookingCard },

  mounted() {
    // eslint-disable-next-line no-undef
    new jsVectorMap({
      selector: "#map",
      map: "world_merc",
      zoomOnScroll: false,
      zoomButtons: false,
      selectedMarkers: [1, 3],
      markersSelectable: true,
      markers: [
        {
          name: "USA",
          coords: [40.71296415909766, -74.00437720027804],
        },
        {
          name: "Germany",
          coords: [51.17661451970939, 10.97947735117339],
        },
        {
          name: "Brazil",
          coords: [-7.596735421549542, -54.781694323779185],
        },
        {
          name: "Russia",
          coords: [62.318222797104276, 89.81564777631716],
        },
        {
          name: "China",
          coords: [22.320178999475512, 114.17161225541399],
          style: {
            fill: "#E91E63",
          },
        },
      ],
      markerStyle: {
        initial: {
          fill: "#e91e63",
        },
        hover: {
          fill: "E91E63",
        },
        selected: {
          fill: "E91E63",
        },
      },
    });
  },
};
</script>
