<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  treemapChart,
  multiSeriesChart,
  distributedChart,
  colorRangeChart,
} from "./data";

/**
 * Treemap chart
 */
export default {
  page: {
    title: "Treemap Charts",
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
      treemapChart: treemapChart,
      multiSeriesChart: multiSeriesChart,
      distributedChart: distributedChart,
      colorRangeChart: colorRangeChart,
      title: "Treemaps Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Treemaps Charts",
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
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Basic Treemap Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="treemapChart.series"
              :options="treemapChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Multi-Dimensional Treemap Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="multiSeriesChart.series"
              :options="multiSeriesChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>
              Distributed Treemap Chart (Different Color for each Cell)
            </b-card-title>

          </b-card-header>

          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="distributedChart.series"
              :options="distributedChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Treemap Chart with Color Ranges</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="colorRangeChart.series"
              :options="colorRangeChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
