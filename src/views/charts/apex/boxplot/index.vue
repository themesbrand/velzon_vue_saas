<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import { boxChart, boxplotScatterChart } from "./data";

/**
 * Boxplot Charts component
 */
export default {
  page: {
    title: "Boxplot Charts",
    meta: [
      {
        name: "description",
        content: appConfig.description,
      },
    ],
  },
  components: {
    Layout,
    PageHeader
  },
  data() {
    return {
      boxChart: boxChart,
      boxplotScatterChart: boxplotScatterChart,
      title: "Boxplot Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Boxplot Charts",
          active: true,
        },
      ],
    };
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="
              justify-content-between
              d-flex
              align-items-center
            ">
            <b-card-title>Basic Candlestick Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="boxChart.series"
              :options="boxChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="
              justify-content-between
              d-flex
              align-items-center
            ">
            <b-card-title>Candlestick Synced with Brush Chart (Combo)</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="boxplotScatterChart.series"
              :options="boxplotScatterChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>