<template>
  <div class="container-fluid py-4">
    <div class="row">
      <div class="col-lg-4 col-sm-7">
        <events-card />
      </div>
      <div class="col-lg-8 mt-lg-0 mt-4">
        <tasks-card />
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-lg-3 col-sm-6">
        <card
          class="bg-gradient-white p-0"
          title="Battery Health"
          value="99 %"
          iconClass="text-white"
          titleColor="opacity-7 text-dark"
          valueColor="text-dark"
          iconBackground="bg-gradient-success"
          iconName="battery_charging_full"
        />
        <card
          class="bg-gradient-white p-0"
          title="Music Volume"
          value="15/100"
          iconClass="text-white"
          titleColor="opacity-7 text-dark"
          valueColor="text-dark"
          iconBackground="bg-gradient-success"
          iconName="volume_down"
        />
      </div>
      <div class="col-lg-5 col-sm-6 mt-sm-0 mt-4">
        <div class="row">
          <div class="col-md-6">
            <default-info-card
              classIcon="text-white"
              title="Salary"
              desc="Belong Interactive"
              price="+$2000"
              iconName="account_balance"
            />
          </div>
          <div class="col-md-6">
            <default-info-card
              classIcon="text-white"
              title="Paypal"
              desc="Freelance Payment"
              price="$455.00"
              iconName="account_balance_wallet"
            />
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <master-card />
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-lg-3 col-md-6">
        <full-body-card />
      </div>
      <div class="col-lg-2 col-md-6">
        <controller-card />
      </div>
      <div class="col-lg-3">
        <calories-chart />
      </div>
      <div class="col-lg-2 col-md-6">
        <mini-info-card />
      </div>
      <div class="col-lg-2 col-md-6">
        <steps-card />
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-lg-5">
        <calendar />
      </div>
      <div class="col-lg-3 mt-0">
        <categories-card />
        <music-player />
      </div>
      <div class="col-lg-4">
        <Orders-card />
      </div>
    </div>
  </div>
</template>

<script>
import Card from "@/examples/Cards/Card.vue";
import TasksCard from "./projects/components/TasksCard.vue";
import DefaultInfoCard from "@/examples/Cards/DefaultInfoCard.vue";
import MasterCard from "@/examples/Cards/MasterCard.vue";
import CaloriesChart from "./components/CaloriesChart.vue";
import EventsCard from "./components/EventsCard.vue";
import FullBodyCard from "./components/FullBodyCard.vue";
import ControllerCard from "./components/ControllerCard.vue";
import MiniInfoCard from "./components/MiniInfoCard.vue";
import StepsCard from "./components/StepsCard.vue";
import Calendar from "@/examples/Calendar.vue";
import CategoriesCard from "../dashboards/components/CategoriesCard.vue";
import MusicPlayer from "./components/MusicPlayer.vue";
import OrdersCard from "./components/OrdersCard.vue";

export default {
  name: "Widgets",
  components: {
    Card,
    TasksCard,
    DefaultInfoCard,
    MasterCard,
    CaloriesChart,
    EventsCard,
    FullBodyCard,
    ControllerCard,
    MiniInfoCard,
    StepsCard,
    Calendar,
    CategoriesCard,
    OrdersCard,
    MusicPlayer,
  },
  data() {
    return {
      stats: {
        titleColor: "opacity-7 text-dark",
        descColor: "text-dark",
        health: {
          title: "Battery Health",
          desc: "99 %",
          classIcon: "text-white ",
        },
        volume: {
          title: "Music Volume",
          desc: "15/100",
          classIcon: "text-white",
        },
      },
      salary: {
        classIcon: "text-white",
        title: "Salary",
        desc: "Belong Interactive",
        price: "+$2000",
      },
      paypal: {
        classIcon: "text-white",
        title: "Paypal",
        desc: "Freelance Payment",
        price: "$455.00",
      },
    };
  },
};
</script>
