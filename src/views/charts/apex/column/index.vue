<script>
import Layout from "../../../../layouts/main.vue";
import appConfig from "../../../../../app.config";
import PageHeader from "@/components/page-header";

import {
  basicColumnChart,
  columnDatalabelChart,
  stackedColumnsChart,
  columnStackedChart,
  columnMarkersChart,
  columnRotatedLabel,
  columnNegativeChart,
  rangeColumnChart,
  chartYearOption,
  quarterChartOption,
  distributedColumnchart,
  dynamicQuarterLoadedChart
} from "./data";

/**
 * Column Charts component
 */
export default {
  page: {
    title: "Column chart",
    meta: [
      {
        name: "description",
        content: appConfig.description,
      },
    ],
  },
  data() {
    return {
      basicColumnChart: basicColumnChart,
      columnDatalabelChart: columnDatalabelChart,
      stackedColumnsChart: stackedColumnsChart,
      columnStackedChart: columnStackedChart,
      columnMarkersChart: columnMarkersChart,
      columnRotatedLabel: columnRotatedLabel,
      columnNegativeChart: columnNegativeChart,
      rangeColumnChart: rangeColumnChart,
      chartYearOption: chartYearOption,
      quarterChartOption: quarterChartOption,
      distributedColumnchart: distributedColumnchart,
      dynamicQuarterLoadedChart: dynamicQuarterLoadedChart,
      title: "Column Charts",
      items: [
        {
          text: "Charts",
          href: "/",
        },
        {
          text: "Column Charts",
          active: true,
        },
      ],
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
            <b-card-title>Basic Column Charts</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="basicColumnChart.series"
              :options="basicColumnChart.chartOptions"></apexchart>
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
            <b-card-title>Column with Data Labels</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="columnDatalabelChart.series"
              :options="columnDatalabelChart.chartOptions"></apexchart>
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
            <b-card-title>Stacked Column Charts</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="stackedColumnsChart.series"
              :options="stackedColumnsChart.chartOptions"></apexchart>
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
            <b-card-title>Stacked Column 100</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="columnStackedChart.series"
              :options="columnStackedChart.chartOptions"></apexchart>
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
            <b-card-title>Column with Markers</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="columnMarkersChart.series"
              :options="columnMarkersChart.chartOptions"></apexchart>
            <div id="column_markers" class="apex-charts" dir="ltr"></div>
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
            <b-card-title>Column with Rotated Labels</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="columnRotatedLabel.series"
              :options="columnRotatedLabel.chartOptions"></apexchart>
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
            <b-card-title>Column with Nagetive Values</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="columnNegativeChart.series"
              :options="columnNegativeChart.chartOptions"></apexchart>
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
            <b-card-title>Range Column Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="rangeColumnChart.series"
              :options="rangeColumnChart.chartOptions"></apexchart>
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
            <b-card-title>Dynamic Loaded Chart</b-card-title>

          </b-card-header>
          <b-card-body>
            <div id="dynamicloadedchart-wrap">
              <div id="chart-year">
                <apexchart type="bar" height="330" ref="chart" :options="chartYearOption.chartOptions"
                  :series="chartYearOption.series"></apexchart>
              </div>
              <div id="chart-quarter">
                <apexchart type="bar" height="330" ref="chartQuarter" :options="dynamicQuarterLoadedChart.chartOptions"
                  :series="dynamicQuarterLoadedChart.series"></apexchart>
              </div>
            </div>
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
            <b-card-title>Distributed Columns Charts</b-card-title>

          </b-card-header>
          <b-card-body>
            <apexchart class="apex-charts" height="350" dir="ltr" :series="distributedColumnchart.series"
              :options="distributedColumnchart.chartOptions"></apexchart>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
