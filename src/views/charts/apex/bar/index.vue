<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  basicBarChart,
  customDatalabelsChart,
  stackedBarChart,
  stackedBar100Chart,
  barNegativeChart,
  barMarkersChart,
  reversedBarChart,
  patternedBarChart,
  groupedBarChart,
  barImagesChart,
} from "./data";

/**
 * Bar charts component
 */
export default {
  page: {
    title: "Bar charts",
    meta: [
      {
        name: "description",
        content: appConfig.description
      },
    ],
  },
  data() {
    return {
      title: "Bar Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Bar Charts",
          active: true,
        },
      ],
      basicBarChart: basicBarChart,
      customDatalabelsChart: customDatalabelsChart,
      stackedBarChart: stackedBarChart,
      stackedBar100Chart: stackedBar100Chart,
      barNegativeChart: barNegativeChart,
      barMarkersChart: barMarkersChart,
      reversedBarChart: reversedBarChart,
      patternedBarChart: patternedBarChart,
      groupedBarChart: groupedBarChart,
      barImagesChart: barImagesChart,
    };
  },
  components: {
    Layout,
    PageHeader
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
            <b-card-title>Basic Bar Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="basicBarChart.series"
              :options="basicBarChart.chartOptions"></apexchart>
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
            <b-card-title>Custom DataLabels Bar</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="customDatalabelsChart.series"
              :options="customDatalabelsChart.chartOptions"></apexchart>
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
            <b-card-title>Stacked Bar Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="stackedBarChart.series"
              :options="stackedBarChart.chartOptions"></apexchart>
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
            <b-card-title>Stacked Bars 100</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="stackedBar100Chart.series"
              :options="stackedBar100Chart.chartOptions"></apexchart>
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
            <b-card-title>Bar with Negative Values</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="barNegativeChart.series"
              :options="barNegativeChart.chartOptions"></apexchart>
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
            <b-card-title>Bar with Marker</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="barMarkersChart.series"
              :options="barMarkersChart.chartOptions"></apexchart>
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
            <b-card-title>Reversed Bar Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="reversedBarChart.series"
              :options="reversedBarChart.chartOptions"></apexchart>
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
            <b-card-title>Patterned Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="patternedBarChart.series"
              :options="patternedBarChart.chartOptions"></apexchart>
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
            <b-card-title>Grouped Bar Chart</b-card-title>
          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="groupedBarChart.series"
              :options="groupedBarChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>

    </b-row>
  </Layout>
</template>