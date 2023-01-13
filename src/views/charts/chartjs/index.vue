<script>
import Layout from "../../../layouts/main";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";
import Vue3ChartJs from "@j-t-mcc/vue3-chartjs";

import { line, pie, Doughnut, radar, bar, PolarArea } from "./data";

/**
 * Chartjs-chart component
 */
export default {
  page: {
    title: "Chartjs Charts",
    meta: [{ name: "description", content: appConfig.description }],
  },
  components: {
    Layout,
    PageHeader,
    Vue3ChartJs,
  },
  data() {
    return {
      line: line,
      pie: pie,
      Doughnut: Doughnut,
      radar: radar,
      bar: bar,
      PolarArea: PolarArea,
      title: "Chartjs",
      items: [
        {
          text: "Charts",
          href: "/",
        },
        {
          text: "Chartjs",
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
          <b-card-body>
            <b-card-title class="mb-4">Line Chart</b-card-title>
            <vue3-chart-js class="chartjs-chart" v-bind="{ ...line }"></vue3-chart-js>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Bar Chart</b-card-title>

            <vue3-chart-js class="chartjs-chart" v-bind="{ ...bar }"></vue3-chart-js>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Pie Chart</b-card-title>

            <vue3-chart-js :height="140" class="chartjs-chart" v-bind="{ ...pie }"></vue3-chart-js>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Donut Chart</b-card-title>

            <vue3-chart-js :height="140" class="chartjs-chart" v-bind="{ ...Doughnut }"></vue3-chart-js>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Polar area Chart</b-card-title>

            <vue3-chart-js :height="140" class="chartjs-chart" v-bind="{ ...PolarArea }"></vue3-chart-js>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Radar Chart</b-card-title>

            <vue3-chart-js :height="140" class="chartjs-chart" v-bind="{ ...radar }"></vue3-chart-js>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>