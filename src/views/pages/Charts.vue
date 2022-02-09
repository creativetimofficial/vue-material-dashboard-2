<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-md-6">
        <h5 class="mb-0">Charts</h5>
        <p class="mb-0 text-sm">
          Charts on this page use Chart.js - Simple yet flexible JavaScript
          charting for designers & developers.
        </p>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-md-6 col-12">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-info shadow-info text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">insights</i>
            </div>
            <div class="d-block d-md-flex">
              <div class="me-auto">
                <h6 class="mb-0">Line chart</h6>
                <p class="mb-0 text-sm">Product insights</p>
              </div>
              <span
                class="badge badge-lg badge-dot me-4 d-inline-block text-start"
              >
                <i class="bg-success"></i>
                <span class="text-dark">Organic</span>
              </span>
              <span
                class="badge badge-lg badge-dot me-4 d-inline-block text-start"
              >
                <i class="bg-dark"></i>
                <span class="text-dark">Refferal</span>
              </span>
              <span
                class="badge badge-lg badge-dot me-4 d-inline-block text-start"
              >
                <i class="bg-info"></i>
                <span class="text-dark">Direct</span>
              </span>
            </div>
          </div>
          <div class="p-3 card-body">
            <div class="chart">
              <line-chart />
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-12 mt-md-0 mt-4">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-info shadow-info text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">show_chart</i>
            </div>
            <div class="d-block d-md-flex">
              <div class="me-auto">
                <h6 class="mb-0">Line chart without dots</h6>
                <p class="mb-0 text-sm">Visits from devices</p>
              </div>
              <span
                class="badge badge-lg badge-dot me-4 d-inline-block text-start"
              >
                <i class="bg-success"></i>
                <span class="text-dark">Mobile Apps</span>
              </span>
              <span
                class="badge badge-lg badge-dot me-4 d-inline-block text-start"
              >
                <i class="bg-dark"></i>
                <span class="text-dark">Websites</span>
              </span>
            </div>
          </div>
          <div class="p-3 card-body">
            <div class="chart">
              <line-chart-gradient />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-md-6 col-12">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-dark shadow-dark text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">leaderboard</i>
            </div>
            <h6 class="mb-0">Bar chart</h6>
            <p class="mb-0 text-sm">Sales related to age average</p>
          </div>
          <div class="p-3 card-body">
            <div class="chart">
              <bar-chart />
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-12 mt-md-0 mt-4">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-dark shadow-dark text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">splitscreen</i>
            </div>
            <h6 class="mb-0">Bar chart horizontal</h6>
            <p class="mb-0 text-sm">Sales related to age average</p>
          </div>
          <div class="p-3 card-body">
            <div class="chart">
              <bar-chart-horizontal />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-md-6 col-12">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-success shadow-primary text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">auto_graph</i>
            </div>
            <h6 class="mb-0">Mixed chart</h6>
            <p class="mb-0 text-sm">Analytics Insights</p>
          </div>
          <div class="p-3 card-body">
            <div class="chart">
              <mixed-chart />
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-12 mt-md-0 mt-4">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-success shadow-primary text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">multiline_chart</i>
            </div>
            <h6 class="mb-0">Bubble chart</h6>
            <p class="mb-0 text-sm">Users divided by regions</p>
          </div>
          <div class="p-3 card-body">
            <div class="chart">
              <bubble-chart />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-md-6 col-12">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-warning shadow-warning text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">donut_small</i>
            </div>
            <h6 class="mb-0">Doughnut chart</h6>
            <p class="mb-0 text-sm">Affiliates program</p>
          </div>
          <div class="p-3 card-body">
            <div class="card-body d-flex p-3 pt-0">
              <div class="chart w-50">
                <doughnut-chart />
              </div>
              <div class="table-responsive w-50">
                <table class="table align-items-center mb-0">
                  <tbody>
                    <tr>
                      <td>
                        <div class="d-flex px-2 py-1">
                          <div>
                            <img
                              src="../../assets/img/small-logos/devto.svg"
                              class="avatar avatar-sm me-2"
                              alt="logo_xd"
                            />
                          </div>
                          <div
                            class="d-flex flex-column justify-content-center"
                          >
                            <h6 class="mb-0 text-sm">DevTo</h6>
                          </div>
                        </div>
                      </td>
                      <td class="align-middle text-center text-sm">
                        <span class="text-xs font-weight-bold">25%</span>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-flex px-2 py-1">
                          <div>
                            <img
                              src="../../assets/img/small-logos/creative-tim.svg"
                              class="avatar avatar-sm me-2"
                              alt="logo_atlassian"
                            />
                          </div>
                          <div
                            class="d-flex flex-column justify-content-center"
                          >
                            <h6 class="mb-0 text-sm">CreativeTim</h6>
                          </div>
                        </div>
                      </td>
                      <td class="align-middle text-center text-sm">
                        <span class="text-xs font-weight-bold">13%</span>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-flex px-2 py-1">
                          <div>
                            <img
                              src="../../assets/img/small-logos/bootstrap.svg"
                              class="avatar avatar-sm me-2"
                              alt="logo_slack"
                            />
                          </div>
                          <div
                            class="d-flex flex-column justify-content-center"
                          >
                            <h6 class="mb-0 text-sm">Bootsnip</h6>
                          </div>
                        </div>
                      </td>
                      <td class="align-middle text-center text-sm">
                        <span class="text-xs font-weight-bold">12%</span>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-flex px-2 py-1">
                          <div>
                            <img
                              src="../../assets/img/small-logos/github.svg"
                              class="avatar avatar-sm me-2"
                              alt="logo_spotify"
                            />
                          </div>
                          <div
                            class="d-flex flex-column justify-content-center"
                          >
                            <h6 class="mb-0 text-sm">Github</h6>
                          </div>
                        </div>
                      </td>
                      <td class="align-middle text-center text-sm">
                        <span class="text-xs font-weight-bold">37%</span>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-flex px-2 py-1">
                          <div>
                            <img
                              src="../../assets/img/small-logos/google-webdev.svg"
                              class="avatar avatar-sm me-2"
                              alt="logo_jira"
                            />
                          </div>
                          <div
                            class="d-flex flex-column justify-content-center"
                          >
                            <h6 class="mb-0 text-sm">Codeinwp</h6>
                          </div>
                        </div>
                      </td>
                      <td class="align-middle text-center text-sm">
                        <span class="text-xs font-weight-bold">13%</span>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-6 col-12 mt-md-0 mt-4">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-warning shadow-warning text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">pie_chart</i>
            </div>
            <h6 class="mb-0">Pie chart</h6>
            <p class="mb-0 text-sm">Analytics Insights</p>
          </div>
          <div class="p-3 card-body">
            <div class="card-body d-flex p-3 pt-0">
              <div class="chart w-50">
                <pie-chart />
              </div>
              <div class="w-50 my-auto ms-5">
                <span class="badge badge-lg badge-dot me-4 d-block text-start">
                  <i class="bg-info"></i>
                  <span class="text-dark">Facebook</span>
                </span>
                <span class="badge badge-lg badge-dot me-4 d-block text-start">
                  <i class="bg-success"></i>
                  <span class="text-dark">Direct</span>
                </span>
                <span class="badge badge-lg badge-dot me-4 d-block text-start">
                  <i class="bg-dark"></i>
                  <span class="text-dark">Organic</span>
                </span>
                <span class="badge badge-lg badge-dot me-4 d-block text-start">
                  <i class="bg-secondary"></i>
                  <span class="text-dark">Referral</span>
                </span>
                <p class="text-sm mt-3">
                  More than
                  <b>1,200,000</b> sales are made using referral marketing, and
                  <b>700,000</b> are from social media.
                </p>
                <a class="btn bg-gradient-secondary mb-0" href="javascript:;"
                  >Read more</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-md-6">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-success shadow-success text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">data_saver_on</i>
            </div>
            <h6 class="mb-0">Radar chart</h6>
            <p class="mb-0 text-sm">Sciences score</p>
          </div>
          <div class="p-5 card-body">
            <div class="chart">
              <radar-chart />
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6 mt-md-0 mt-4">
        <div class="card z-index-2 mt-4">
          <div class="card-header p-3 pt-2">
            <div
              class="icon icon-lg icon-shape bg-gradient-success shadow-success text-center border-radius-xl mt-n4 me-3 float-start"
            >
              <i class="material-icons opacity-10">scatter_plot</i>
            </div>
            <h6 class="mb-0">Polar chart</h6>
            <p class="mb-0 text-sm">Analytics Insights</p>
          </div>
          <div class="p-5 card-body">
            <div class="chart">
              <polar-chart />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LineChart from "./components/LineChart.vue";
import LineChartGradient from "./components/LineChartGradient.vue";
import BarChart from "./components/BarChart.vue";
import BarChartHorizontal from "./components/BarChartHorizontal.vue";
import MixedChart from "./components/MixedChart.vue";
import BubbleChart from "./components/BubbleChart.vue";
import DoughnutChart from "./components/DoughnutChart.vue";
import PieChart from "./components/PieChart.vue";
import RadarChart from "./components/RadarChart.vue";
import PolarChart from "./components/PolarChart.vue";

export default {
  name: "charts",
  components: {
    LineChart,
    LineChartGradient,
    BarChart,
    BarChartHorizontal,
    MixedChart,
    BubbleChart,
    DoughnutChart,
    PieChart,
    RadarChart,
    PolarChart,
  },
};
</script>
