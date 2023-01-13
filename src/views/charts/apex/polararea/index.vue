<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import { basicPolarareaChart, polarAreaMonochromeChart } from "./data";

/**
 * Polararea chart component
 */
export default {
  page: {
    title: "Polararea Charts",
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
      basicPolarareaChart: basicPolarareaChart,
      polarAreaMonochromeChart: polarAreaMonochromeChart,
      title: "Polararea Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Polararea Charts",
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
            <b-card-title>Basic-Polar Area Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="330" dir="ltr" :series="basicPolarareaChart.series"
              :options="basicPolarareaChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Polar-Area Monochrome</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="330" dir="ltr" :series="polarAreaMonochromeChart.series"
              :options="polarAreaMonochromeChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
