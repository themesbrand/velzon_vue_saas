<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  simplePieChart,
  donutChart,
  updatingDonutChart,
  gradientDonutChart,
  patternDonutChart,
  imagePieChart,
  monochromePieChart,
} from "./data";

/**
 * Pie chart component
 */
export default {
  page: {
    title: "Pie Charts",
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
      simplePieChart: simplePieChart,
      donutChart: donutChart,
      updatingDonutChart: updatingDonutChart,
      gradientDonutChart: gradientDonutChart,
      patternDonutChart: patternDonutChart,
      imagePieChart: imagePieChart,
      monochromePieChart: monochromePieChart,
      title: "Pie Charts",
      items: [
        {
          text: "Apexcharts",
          href: "/",
        },
        {
          text: "Pie Charts",
          active: true,
        },
      ],
    };
  },
  methods: {
    appendData: function () {
      var arr = this.updatingDonutChart.series.slice();
      arr.push(Math.floor(Math.random() * (100 - 1 + 1)) + 1);
      this.updatingDonutChart.series = arr;
    },

    removeData: function () {
      if (this.updatingDonutChart.series.length === 1) return;
      var arr = this.updatingDonutChart.series.slice();
      arr.pop();
      this.updatingDonutChart.series = arr;
    },

    randomize: function () {
      this.updatingDonutChart.series = this.updatingDonutChart.series.map(function () {
        return Math.floor(Math.random() * (100 - 1 + 1)) + 1;
      });
    },

    reset: function () {
      this.updatingDonutChart.series = [44, 55, 13, 33];
    },
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
            <b-card-title>Simple Pie Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="simplePieChart.series"
              :options="simplePieChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Simple Donut Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="donutChart.series"
              :options="donutChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Updating Donut Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="updatingDonutChart.series"
              :options="updatingDonutChart.chartOptions"></apexchart>

            <div class="d-flex align-items-start flex-wrap gap-2 justify-content-center mt-4">
              <b-button id="add" variant="light" size="sm" @click="appendData">
                + ADD
              </b-button>

              <b-button id="remove" variant="light" size="sm" @click="removeData">
                - REMOVE
              </b-button>

              <b-button id="randomize" variant="light" size="sm" @click="randomize">
                RANDOMIZE
              </b-button>

              <b-button id="reset" variant="light" size="sm" @click="reset">
                RESET
              </b-button>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Monochrome Pie Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="monochromePieChart.series"
              :options="monochromePieChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Gradient Donut Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="gradientDonutChart.series"
              :options="gradientDonutChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Patterned Donut Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="patternDonutChart.series"
              :options="patternDonutChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-header class="justify-content-between d-flex align-items-center">
            <b-card-title>Pie Chart with Image Fill</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="300" dir="ltr" :series="imagePieChart.series"
              :options="imagePieChart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
