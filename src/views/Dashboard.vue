<template>
  <div class="py-4 container-fluid">
    <div class="row mb-4">
      <div class="col-lg-12 position-relative z-index-2">
        <div class="row">
          <div class="col-lg-3 col-md-6 col-sm-6">
            <mini-statistics-card
              :title="{ text: 'Today\'s Money', value: '$53k' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+55%</span> than last week"
              :icon="{
                name: 'weekend',
                color: 'text-white',
                background: 'dark',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'Today\'s Users', value: '2,300' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+3%</span> than last month"
              :icon="{
                name: 'leaderboard',
                color: 'text-white',
                background: 'primary',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'New Clients', value: '3,462' }"
              detail="<span class='text-danger text-sm font-weight-bolder'>-2%</span> than yesterday"
              :icon="{
                name: 'person',
                color: 'text-white',
                background: 'success',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'Sales', value: '$103,430' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+5%</span> Just updated"
              :icon="{
                name: 'weekend',
                color: 'text-white',
                background: 'info',
              }"
            />
          </div>
        </div>
        <div class="row mt-4">
          <div class="col-lg-4 col-md-6 mt-4">
            <chart-holder-card
              title="Website Views"
              subtitle="Last Campaign Performance"
              update="campaign sent 2 days ago"
            >
              <reports-bar-chart
                :chart="{
                  labels: ['M', 'T', 'W', 'T', 'F', 'S', 'S'],
                  datasets: {
                    label: 'Sales',
                    data: [50, 20, 10, 22, 50, 10, 40],
                  },
                }"
              />
            </chart-holder-card>
          </div>
          <div class="col-lg-4 col-md-6 mt-4">
            <chart-holder-card
              title="Daily Sales"
              subtitle="(<span class='font-weight-bolder'>+15%</span>) increase in today sales."
              update="updated 4 min ago"
              color="success"
            >
              <reports-line-chart
                :chart="{
                  labels: [
                    'Apr',
                    'May',
                    'Jun',
                    'Jul',
                    'Aug',
                    'Sep',
                    'Oct',
                    'Nov',
                    'Dec',
                  ],
                  datasets: {
                    label: 'Mobile apps',
                    data: [50, 40, 300, 320, 500, 350, 200, 230, 500],
                  },
                }"
              />
            </chart-holder-card>
          </div>
          <div class="col-lg-4 mt-4">
            <chart-holder-card
              title="Completed Tasks"
              subtitle="Last Campaign Performance"
              update="just updated"
              color="dark"
            >
              <reports-line-chart
                id="tasks-chart"
                :chart="{
                  labels: [
                    'Apr',
                    'May',
                    'Jun',
                    'Jul',
                    'Aug',
                    'Sep',
                    'Oct',
                    'Nov',
                    'Dec',
                  ],
                  datasets: {
                    label: 'Mobile apps',
                    data: [50, 40, 300, 220, 500, 250, 400, 230, 500],
                  },
                }"
              />
            </chart-holder-card>
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-lg-8 col-md-6 mb-md-0 mb-4">
        <project-card
          title="Projects"
          description="<i class='fa fa-check text-info' aria-hidden='true'></i> <span class='font-weight-bold ms-1'>30 done</span> this month"
          :headers="['Companies', 'Members', 'Budget', 'Progress']"
          :projects="[
            {
              logo: logoXD,
              title: 'Material XD Material XD Version',
              members: [team1, team2, team3, team4],
              budget: '$14,000',
              progress: { percentage: 60, color: 'info' },
            },
            {
              logo: logoAtlassian,
              title: 'Add Progress Track',
              members: [team2, team4],
              budget: '$3,000',
              progress: { percentage: 10, color: 'info' },
            },
            {
              logo: logoSlack,
              title: 'Fix Platform Errors',
              members: [team3, team1],
              budget: 'Not set',
              progress: { percentage: 100, color: 'success' },
            },
            {
              logo: logoSpotify,
              title: 'Launch our Mobile App',
              members: [team4, team3, team4, team1],
              budget: '$20,500',
              progress: { percentage: 100, color: 'success' },
            },
            {
              logo: logoJira,
              title: 'Add the New Pricing Page',
              members: [team4],
              budget: '$500',
              progress: { percentage: 25, color: 'info' },
            },
            {
              logo: logoJira,
              title: 'Redesign New Online Shop',
              members: [team1, team4],
              budget: '$2,000',
              progress: { percentage: 40, color: 'info' },
            },
          ]"
        />
      </div>
      <div class="col-lg-4 col-md-6">
        <orders-card />
      </div>
    </div>
  </div>
</template>
<script>
import ChartHolderCard from "./components/ChartHolderCard.vue";
import ReportsBarChart from "@/examples/Charts/ReportsBarChart.vue";
import ReportsLineChart from "@/examples/Charts/ReportsLineChart.vue";
import MiniStatisticsCard from "./components/MiniStatisticsCard.vue";
import ProjectCard from "./components/ProjectCard.vue";
import OrdersCard from "./components/OrdersCard.vue";
import logoXD from "@/assets/img/small-logos/logo-xd.svg";
import logoAtlassian from "@/assets/img/small-logos/logo-atlassian.svg";
import logoSlack from "@/assets/img/small-logos/logo-slack.svg";
import logoSpotify from "@/assets/img/small-logos/logo-spotify.svg";
import logoJira from "@/assets/img/small-logos/logo-jira.svg";
import logoInvision from "@/assets/img/small-logos/logo-invision.svg";
import team1 from "@/assets/img/team-1.jpg";
import team2 from "@/assets/img/team-2.jpg";
import team3 from "@/assets/img/team-3.jpg";
import team4 from "@/assets/img/team-4.jpg";
export default {
  name: "dashboard-default",
  data() {
    return {
      logoXD,
      team1,
      team2,
      team3,
      team4,
      logoAtlassian,
      logoSlack,
      logoSpotify,
      logoJira,
      logoInvision,
    };
  },
  components: {
    ChartHolderCard,
    ReportsBarChart,
    ReportsLineChart,
    MiniStatisticsCard,
    ProjectCard,
    OrdersCard,
  },
};
</script>
