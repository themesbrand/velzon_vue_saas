<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  basicCandlestickChart,
  comboCandlestickBrushChart,
  comboCandlestickChart,
  categoryXaxisChart,
} from "./data";

/**
 * Candlestick Charts component
 */
export default {
  page: {
    title: "Candlestick Charts",
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
      basicCandlestickChart: basicCandlestickChart,
      comboCandlestickBrushChart: comboCandlestickBrushChart,
      comboCandlestickChart: comboCandlestickChart,
      categoryXaxisChart: categoryXaxisChart,
      title: "Candlestick Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Candlestick Charts",
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
            <apexchart class="apex-charts" height="350" dir="ltr" :series="basicCandlestickChart.series"
              :options="basicCandlestickChart.chartOptions"></apexchart>
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
            <apexchart class="apex-charts" height="200" dir="ltr" :series="comboCandlestickBrushChart.series"
              :options="comboCandlestickBrushChart.chartOptions"></apexchart>
            <apexchart class="apex-charts" height="150" dir="ltr" :series="comboCandlestickChart.series"
              :options="comboCandlestickChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="
              justify-content-between
              d-flex
              align-items-center
            ">
            <b-card-title>Category X-Axis</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="categoryXaxisChart.series"
              :options="categoryXaxisChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>