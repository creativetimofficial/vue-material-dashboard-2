<template>
  <div class="py-4 container-fluid">
    <div class="row mb-4">
      <div class="col-lg-12 position-relative z-index-2">
        <div class="row">
          <div class="col-lg-3 col-md-6 col-sm-6">
            <mini-statistics-card
              :title="{ text: 'Bookings', value: 281 }"
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
              :title="{ text: 'Revenue', value: '34k' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+1%</span> than yesterday"
              :icon="{
                name: 'leaderboard',
                color: 'text-white',
                background: 'success',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'Followers', value: '+91' }"
              detail="Just updated"
              :icon="{
                name: 'person_add',
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
          description='<i class="fa fa-check text-info" aria-hidden="true"></i>
            <span class="font-weight-bold ms-1">30 done</span>
            this month'
          :headings="['COMPANIES', 'MEMBERS', 'BUDGET', 'PROGRESS']"
          :rows="[
            {
              logo: logoXD,
              tool: 'Material XD Version',
              teamMembers: [team1, team2, team3, team4],
              price: '$14,000',
              progress: 60,
            },
            {
              logo: logoAtlassian,
              tool: 'Add Progress Track',
              teamMembers: [team1, team2],
              price: '$3,000',
              progress: 10,
            },
            {
              logo: logoSlack,
              tool: 'Fix Platform Errors',
              teamMembers: [team2, team4],
              price: 'غير مضبوط',
              progress: 100,
            },
            {
              logo: logoSpotify,
              tool: 'Launch our Mobile App',
              teamMembers: [team1, team2, team3, team4],
              price: '$20,500',
              progress: 60,
            },
            {
              logo: logoJira,
              tool: 'Add the New Pricing Page',
              teamMembers: [team1],
              price: '$500',
              progress: 25,
            },
            {
              logo: logoInvision,
              tool: 'Redesign New Online Shop',
              teamMembers: [team1, team4],
              price: '$2,000',
              progress: 40,
            },
          ]"
          :action="[
            {
              route: 'javascript:;',
              label: 'action',
            },
            {
              route: 'javascript:;',
              label: 'Another action',
            },
            {
              route: 'javascript:;',
              label: 'Read more',
            },
          ]"
        />
      </div>
      <div class="col-lg-4 col-md-6">
        <timeline-list
          class="h-100"
          title="Orders overview"
          description="<i class='fa fa-arrow-up text-success' aria-hidden='true'></i>
        <span class='font-weight-bold'>24%</span> this month"
        >
          <timeline-item
            :icon="{
              component: 'notifications',
              class: 'text-success',
            }"
            title="$2400 Design changes"
            date-time="22 DEC 7:20 PM"
          />
          <TimelineItem
            :icon="{
              component: 'code',
              class: 'text-danger',
            }"
            title="New order #1832412"
            date-time="21 DEC 11 PM"
          />
          <TimelineItem
            :icon="{
              component: 'shopping_cart',
              class: 'text-info',
            }"
            title="Server payments for April"
            date-time="21 DEC 9:34 PM"
          />
          <TimelineItem
            :icon="{
              component: 'credit_card',
              class: 'text-warning',
            }"
            title="New card added for order #4395133"
            date-time="20 DEC 2:20 AM"
          />
          <TimelineItem
            :icon="{
              component: 'vpn_key',
              class: 'text-primary',
            }"
            title="Unlock packages for development"
            date-time="18 DEC 4:54 AM"
            class="pb-1"
          />
        </timeline-list>
      </div>
    </div>
  </div>
</template>
<script>
import ChartHolderCard from "./components/ChartHolderCard.vue";
import ReportsBarChart from "@/examples/Charts/ReportsBarChart.vue";
import ReportsLineChart from "@/examples/Charts/ReportsLineChart.vue";
import MiniStatisticsCard from "@/examples/Cards/MiniStatisticsCard.vue";
import ProjectCard from "./components/ProjectCard.vue";
import TimelineList from "@/examples/Cards/TimelineList.vue";
import TimelineItem from "@/examples/Cards/TimelineItem.vue";

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
      logoAtlassian,
      logoSlack,
      logoSpotify,
      logoJira,
      logoInvision,
      team1,
      team2,
      team3,
      team4,
    };
  },
  components: {
    ChartHolderCard,
    ReportsBarChart,
    ReportsLineChart,
    MiniStatisticsCard,
    ProjectCard,
    TimelineList,
    TimelineItem,
  },
};
</script>
