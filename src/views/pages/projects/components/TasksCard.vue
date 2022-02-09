<template>
  <div class="overflow-hidden card">
    <div class="p-3 pb-0 card-header">
      <div class="d-flex align-items-center">
        <div
          class="text-center shadow icon icon-shape border-radius-md"
          :class="bgColor"
        >
          <i class="text-lg opacity-10 material-icons" aria-hidden="true"
            >today</i
          >
        </div>
        <div :class="this.$store.state.isRTL ? 'me-3' : 'ms-3'">
          <p class="mb-0 text-sm text-capitalize">{{ title }}</p>
          <h5 class="mb-0 font-weight-bolder">480</h5>
        </div>
        <div
          class="progress-wrapper w-25"
          :class="this.$store.state.isRTL ? 'me-auto' : 'ms-auto'"
        >
          <div class="progress-primary">
            <div class="progress-j">
              <span class="text-xs font-weight-bold">60%</span>
            </div>
          </div>
          <div class="progress">
            <div
              class="progress-bar w-60"
              :class="bgColor"
              role="progressbar"
              aria-valuenow="60"
              aria-valuemin="0"
              aria-valuemax="100"
            ></div>
          </div>
        </div>
      </div>
    </div>
    <div class="p-0 mt-3 card-body">
      <div class="chart">
        <canvas
          id="chart-line-widgets"
          class="chart-canvas"
          height="200"
        ></canvas>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js/auto";

export default {
  name: "tasks-card",
  props: {
    title: {
      type: String,
      default: "Tasks",
    },
    bgColor: {
      type: String,
      default: "bg-gradient-success",
    },
  },
  mounted() {
    var ctx3 = document.getElementById("chart-line-widgets").getContext("2d");

    var gradientStroke3 = ctx3.createLinearGradient(0, 230, 0, 50);

    gradientStroke3.addColorStop(1, "rgba(33,82,255,0.1)");
    gradientStroke3.addColorStop(0.2, "rgba(33,82,255,0.0)");
    gradientStroke3.addColorStop(0, "rgba(33,82,255,0)"); //purple colors

    new Chart(ctx3, {
      type: "line",
      data: {
        labels: ["Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"],
        datasets: [
          {
            label: "Tasks",
            tension: 0,
            pointRadius: 5,
            pointBackgroundColor: "#4caf50",
            pointBorderColor: "transparent",
            borderColor: "#4caf50",
            borderWidth: 4,
            backgroundColor: "transparent",
            data: [40, 45, 42, 41, 40, 43, 40, 42, 39],
            maxBarThickness: 6,
            fill: true,
          },
        ],
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: {
            display: false,
          },
        },
        interaction: {
          intersect: false,
          mode: "index",
        },
        scales: {
          y: {
            grid: {
              drawBorder: false,
              display: false,
              drawOnChartArea: true,
              drawTicks: false,
              borderDash: [5, 5],
            },
            ticks: {
              display: true,
              padding: 10,
              color: "#9ca2b7",
              font: {
                size: 14,
                weight: 300,
                family: "Roboto",
                style: "normal",
                lineHeight: 2,
              },
            },
          },
          x: {
            grid: {
              drawBorder: false,
              display: true,
              drawOnChartArea: true,
              drawTicks: false,
              borderDash: [5, 5],
              color: "#c1c4ce5c",
            },
            ticks: {
              display: true,
              padding: 10,
              color: "#9ca2b7",
              font: {
                size: 14,
                weight: 300,
                family: "Roboto",
                style: "normal",
                lineHeight: 2,
              },
            },
          },
        },
      },
    });
  },
};
</script>
