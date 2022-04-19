<template>
  <div class="py-4 container-fluid">
    <div class="row mb-4">
      <div class="col-lg-12 position-relative z-index-2">
        <div class="row">
          <div class="col-lg-3 col-md-6 col-sm-6">
            <mini-statistics-card
              :title="{ text: 'أموال اليوم', value: '$53k' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+55%</span> من الأسبوع الماضي"
              :icon="{
                name: 'weekend',
                color: 'text-white',
                background: 'dark',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'مستخدمو اليوم', value: '2,300' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+3%</span> من الأسبوع الماضي"
              :icon="{
                name: 'leaderboard',
                color: 'text-white',
                background: 'primary',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'عملاء جدد', value: '34K' }"
              detail="<span class='text-danger text-sm font-weight-bolder'>+1%</span> من الشهر الماضي"
              :icon="{
                name: 'store',
                color: 'text-white',
                background: 'success',
              }"
            />
          </div>
          <div class="col-lg-3 col-md-6 col-sm-6 mt-lg-0 mt-4">
            <mini-statistics-card
              :title="{ text: 'مبيعات', value: '+91' }"
              detail="<span class='text-success text-sm font-weight-bolder'>+5%</span> مقارنة بيوم أمس"
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
            <chart-bars
              title="مشاهدات الموقع"
              desc="آخر أداء للحملة"
              date="الحملة أرسلت قبل يومين"
            />
            <chart-holder-card
              title="مشاهدات الموقع"
              subtitle="آخر أداء للحملة"
              update="الحملة أرسلت قبل يومين"
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
              subtitle="(<span class='font-weight-bolder'>+15%</span>) المبيعات اليومية."
              update="تم التحديث منذ 4 دقائق"
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
              title="المهام المكتملة"
              subtitle="آخر أداء للحملة"
              update="تم تحديثه للتو"
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
        <projects-card
          Action="عمل"
          AnotherAction="عمل اخر"
          SomethingElse="شی اخر هنا"
          th1="المشروع"
          th2="أعضاء"
          th3="ميزانية"
          th4="إكمال"
          title="المشاريع"
          desc="هذا الشهر"
          descBold="انتهى30 "
          data1="الإصدار"
          data2="أضف مسار التقدم إلى التطبيق الداخلي"
          data3="إصلاح أخطاء النظام الأساسي"
          data5="أضف صفحة التسعير الجديدة"
          data6="إعادة تصميم متجر جديد على الإنترنت"
          data4="إطلاق تطبيق الهاتف المحمول الخاص بنا"
          empty="غير مضبوط"
        />
      </div>
      <div class="col-lg-4 col-md-6">
        <orders-card
          title="نظرة عامة على الطلبات"
          text="هذا الشهر"
          order="$2400, تغييرات في التصميم"
          newOrder="طلب جديد #1832412"
          payment="مدفوعات الخادم لشهر أبريل"
          newCard="تمت إضافة بطاقة جديدة للطلب #4395133"
          unlockPackages="فتح الحزم من أجل التطوير"
          newOrder2="طلب جديد #9583120"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ChartHolderCard from "./components/ChartHolderCard.vue";
import ReportsBarChart from "@/examples/Charts/ReportsBarChart.vue";
import ReportsLineChart from "@/examples/Charts/ReportsLineChart.vue";
import MiniStatisticsCard from "./components/MiniStatisticsCard.vue";
import ProjectsCard from "./components/ProjectsCard.vue";
import OrdersCard from "./components/OrdersCard.vue";

export default {
  name: "rtl-page",

  components: {
    ChartHolderCard,
    ReportsBarChart,
    ReportsLineChart,
    MiniStatisticsCard,
    ProjectsCard,
    OrdersCard,
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
