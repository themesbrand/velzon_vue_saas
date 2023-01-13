<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  basicRadialBarChart,
  multiRadialbarChart,
  circleAngleChart,
  gradientRadialbarChart,
  strokedRadialbarChart,
  semiRadialbarChart,
} from "./data";

/**
 * Radaialbar chart component
 */
export default {
  page: {
    title: "Radialbar Charts",
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
      basicRadialBarChart: basicRadialBarChart,
      multiRadialbarChart: multiRadialbarChart,
      circleAngleChart: circleAngleChart,
      gradientRadialbarChart: gradientRadialbarChart,
      strokedRadialbarChart: strokedRadialbarChart,
      semiRadialbarChart: semiRadialbarChart,
      title: "Radialbar Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Radialbar Charts",
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
            <b-card-title>Basic Radialbar Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="basicRadialBarChart.series"
              :options="basicRadialBarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Multiple Radialbar</b-card-title>

          </b-card-header>
          <b-card-body>
            <div id="multiple_radialbar" class="apex-charts" dir="ltr"></div>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="multiRadialbarChart.series"
              :options="multiRadialbarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Circle Chart - Custom Angle</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="circleAngleChart.series"
              :options="circleAngleChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Gradient Circle Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="gradientRadialbarChart.series"
              :options="gradientRadialbarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row class="mb-4">
      <b-col lg="6">
        <b-card no-body class="h-100 mb-xl-0">
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Stroked Circular Gauge</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="strokedRadialbarChart.series"
              :options="strokedRadialbarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body class="h-100 mb-xl-0">
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Semi Circular Gauge</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="semiRadialbarChart.series"
              :options="semiRadialbarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
