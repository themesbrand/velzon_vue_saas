<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  basicRadarChart,
  radarMultiseriesChart,
  polygonRadarChart,
} from "./data";

/**
 * Radar chart component
 */
export default {
  page: {
    title: "Radar Charts",
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
      basicRadarChart: basicRadarChart,
      radarMultiseriesChart: radarMultiseriesChart,
      polygonRadarChart: polygonRadarChart,
      title: "Radar Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Radar Charts",
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
            <b-card-title>Basic Radar Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="basicRadarChart.series"
              :options="basicRadarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Radar Chart - Multiple series</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="radarMultiseriesChart.series"
              :options="radarMultiseriesChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Radar Chart - Polygon Fill</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="polygonRadarChart.series"
              :options="polygonRadarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
