<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import { simpleBubbleChart, bubble3DChart } from "./data";

/**
 * Bubble Charts component
 */
export default {
  page: {
    title: "Bubble Charts",
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
      simpleBubbleChart: simpleBubbleChart,
      bubble3DChart: bubble3DChart,
      title: "Bubble Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Bubble Charts",
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
            <b-card-title>Simple Bubble Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="simpleBubbleChart.series"
              :options="simpleBubbleChart.chartOptions"></apexchart>
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
            <b-card-title>3D Bubble Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="bubble3DChart.series"
              :options="bubble3DChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
