<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-4 col-md-7">
        <events-card
          title="الأحداث القادمة"
          subTitle="انضم"
          eventTitle="أسبوع الإنترنت"
          eventDate="01 يونيو 2021, ي 12:30 PM"
          eventTitle2="لقاء مع ماري"
          eventDate2="24 مايو 2021, ي 10:00 PM"
          eventTitle3="تخطيط المهمة"
          eventDate3="25 مايو 2021, ي 10:00 PM"
        />
      </div>
      <div class="col-lg-8 mt-lg-0 mt-4">
        <tasks-card title="مهام" />
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-lg-3 col-sm-6">
        <card
          directionReverse
          class="p-0 bg-gradient-white"
          title="صحة البطارية"
          value="99 %"
          iconClass="text-white"
          iconBackground="bg-gradient-success"
          titleColor="opacity-7 text-dark"
          valueColor="text-dark"
          iconName="battery_charging_full"
        />
        <card
          directionReverse
          class="p-0 bg-gradient-white"
          title="طبقة صوت الموسيقا"
          value="30/100"
          iconClass="text-white"
          titleColor="opacity-7 text-dark"
          iconBackground="bg-gradient-success"
          valueColor="text-dark"
          iconName="volume_down"
        />
      </div>
      <div class="col-lg-5 col-sm-6 mt-sm-0 mt-4">
        <div class="row">
          <div class="col-md-6">
            <default-info-card
              classIcon="text-white"
              title="مرتب"
              desc="تنتمي التفاعلية"
              price="+$2000"
              iconName="account_balance"
            />
          </div>
          <div class="col-md-6">
            <default-info-card
              classIcon="text-white"
              title="باي بال"
              desc="دفع لحسابهم الخاص"
              price="$455.00"
              iconName="account_balance_wallet"
            />
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <master-card
          cardHolderText="حامل البطاقة"
          name="جاك بيترسون"
          cardExpirationText="نتهي"
        />
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-lg-3 col-md-6">
        <full-body-card
          title="جسم كامل"
          badgeText="معتدل"
          description="ما يهم هو الأشخاص الذين أوقدوه. والناس الذين يشبهونهم مستاءون منه."
        />
      </div>
      <div class="col-lg-2 col-md-6">
        <controller-card controllerIs="على" text="درجة حرارة" />
      </div>
      <div class="col-lg-3">
        <calories-chart title="سعرات حراريه" />
      </div>
      <div class="col-lg-2 col-md-6">
        <mini-info-card unit="م" location="مدينة نيويورك" />
      </div>
      <div class="col-lg-2 col-md-6">
        <steps-card title="خطوات" steps="11.4ک" />
      </div>
    </div>
    <div class="mt-4 row">
      <div class="col-lg-5">
        <calendar title="تقویم" />
      </div>
      <div class="mt-0 col-lg-3">
        <categories-card
          cardTitle="فئات"
          title="الأجهزة"
          titleDesc="250 في المخزن"
          titleDesc2="346+ تم البيع"
          title2="تذاكر"
          title2Desc="123 مغلق"
          title2Desc2="15 افتح"
          title3="سجلات الخطأ"
          title3Desc="1 is نشيط"
          title3Desc2="40 مغلق"
          title4="المستخدمين السعداء"
          title4Desc2="+ 430"
        />
        <music-player title="نوع من البلوز" desc="ديفتونز" />
      </div>
      <div class="col-lg-4">
        <Orders-card
          title="نظرة عامة على الطلبات"
          text="هذا الشهر"
          order="$2400, تغييرات في التصميم"
          date="22 ديسمبر 7:20 مساءً"
          newOrder="طلب جديد # 1832412"
          orderDate="21 ديسمبر 11 م"
          payment="مدفوعات الخادم لشهر أبريل"
          paymentDate="21 ديسمبر 9:34 مساءً"
          newCard="تمت إضافة بطاقة جديدة للأمر رقم 4395133"
          newCardDate="20 ديسمبر 2:20 صباحًا"
          unlockPackages="فتح الحزم من أجل التطوير"
          unlockPackagesDate="18 ديسمبر ، 4:54 صباحًا"
          newOrder2="طلب جديد # 9583120"
          newOrder2Date="17 ديسمبر"
        />
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
import CategoriesCard from "@/views/dashboards/components/CategoriesCard.vue";
import MusicPlayer from "./components/MusicPlayer.vue";
import OrdersCard from "./components/OrdersCard.vue";

export default {
  name: "rtl-page",
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
  beforeMount() {
    this.$store.state.isRTL = true;
    document.querySelector("html").setAttribute("lang", "ar");
    document.querySelector("html").setAttribute("dir", "rtl");
    document.querySelector("#app").classList.add("rtl");
  },
  beforeUnmount() {
    this.$store.state.isRTL = false;
    document.querySelector("html").removeAttribute("lang");
    document.querySelector("html").removeAttribute("dir");
    document.querySelector("#app").classList.remove("rtl");
  },
};
</script>
