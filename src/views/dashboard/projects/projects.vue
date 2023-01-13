<script>
import {
  CountTo
} from "vue3-count-to";

function getChartColorsArray(colors) {
  colors = JSON.parse(colors);
  return colors.map(function (value) {
    var newValue = value.replace(" ", "");
    if (newValue.indexOf(",") === -1) {
      var color = getComputedStyle(document.documentElement).getPropertyValue(newValue);
      if (color) {
        color = color.replace(" ", "");
        return color;
      } else return newValue;
    } else {
      var val = value.split(',');
      if (val.length == 2) {
        var rgbaColor = getComputedStyle(document.documentElement).getPropertyValue(val[0]);
        rgbaColor = "rgba(" + rgbaColor + "," + val[1] + ")";
        return rgbaColor;
      } else {
        return newValue;
      }
    }
  });
}

export default {
  components: {
    CountTo
  },
  setup() {
    return {
      series: [{
        name: "Number of Projects",
        type: "bar",
        data: [34, 65, 46, 68, 49, 61, 42, 44, 78, 52, 63, 67],
      },
      {
        name: "Revenue",
        type: "area",
        data: [
          89.25, 98.58, 68.74, 108.87, 77.54, 84.03, 51.24, 28.57, 92.57,
          42.36, 88.51, 36.57,
        ],
      },
      {
        name: "Active Projects",
        type: "bar",
        data: [8, 12, 7, 17, 21, 11, 5, 9, 7, 29, 12, 35],
      },
      ],
      chartOptions: {
        chart: {
          height: 374,
          type: "line",
          toolbar: {
            show: false,
          },
        },
        stroke: {
          curve: "smooth",
          dashArray: [0, 3, 0],
          width: [0, 1, 0],
        },
        fill: {
          opacity: [1, 0.1, 1],
        },
        markers: {
          size: [0, 4, 0],
          strokeWidth: 2,
          hover: {
            size: 4,
          },
        },
        xaxis: {
          categories: [
            "Jan",
            "Feb",
            "Mar",
            "Apr",
            "May",
            "Jun",
            "Jul",
            "Aug",
            "Sep",
            "Oct",
            "Nov",
            "Dec",
          ],
          axisTicks: {
            show: false,
          },
          axisBorder: {
            show: false,
          },
        },
        grid: {
          show: true,
          xaxis: {
            lines: {
              show: true,
            },
          },
          yaxis: {
            lines: {
              show: false,
            },
          },
          padding: {
            top: 0,
            right: -2,
            bottom: 15,
            left: 10,
          },
        },
        legend: {
          show: true,
          horizontalAlign: "center",
          offsetX: 0,
          offsetY: -5,
          markers: {
            width: 9,
            height: 9,
            radius: 6,
          },
          itemMargin: {
            horizontal: 10,
            vertical: 0,
          },
        },
        plotOptions: {
          bar: {
            columnWidth: "30%",
            barHeight: "70%",
          },
        },
        colors: getChartColorsArray('["--vz-primary", "--vz-warning", "--vz-success"]'),
        tooltip: {
          shared: true,
          y: [{
            formatter: function (y) {
              if (typeof y !== "undefined") {
                return y.toFixed(0);
              }
              return y;
            },
          },
          {
            formatter: function (y) {
              if (typeof y !== "undefined") {
                return "$" + y.toFixed(2) + "k";
              }
              return y;
            },
          },
          {
            formatter: function (y) {
              if (typeof y !== "undefined") {
                return y.toFixed(0);
              }
              return y;
            },
          },
          ],
        },
      },
    };
  },
};
</script>

<template>
  <b-card no-body>
    <b-card-header class="border-0 align-items-center d-flex">
      <b-card-title class="mb-0 flex-grow-1">Projects Overview</b-card-title>
      <div class="hstack gap-1">
        <b-button type="button" variant="soft-secondary" size="sm">ALL</b-button>
        <b-button type="button" variant="soft-secondary" size="sm">1M</b-button>
        <b-button type="button" variant="soft-secondary" size="sm">6M</b-button>
        <b-button type="button" variant="soft-primary" size="sm">1Y</b-button>
      </div>
    </b-card-header>

    <b-card-header class="p-0 border-0 bg-soft-light">
      <b-row class="g-0 text-center">
        <b-col cols="6" sm="3">
          <div class="p-3 border border-dashed border-start-0">
            <h5 class="mb-1">
              <count-to :duration="1000" :startVal='0' :endVal="9851"></count-to>
            </h5>
            <p class="text-muted mb-0">Number of Projects</p>
          </div>
        </b-col>
        <b-col cols="6" sm="3">
          <div class="p-3 border border-dashed border-start-0">
            <h5 class="mb-1">
              <count-to :duration="1000" :startVal='0' :endVal="1026"></count-to>
            </h5>
            <p class="text-muted mb-0">Active Projects</p>
          </div>
        </b-col>
        <b-col cols="6" sm="3">
          <div class="p-3 border border-dashed border-start-0">
            <h5 class="mb-1">
              $<count-to :duration="1000" :startVal='0' :endVal="228"></count-to>k
            </h5>
            <p class="text-muted mb-0">Revenue</p>
          </div>
        </b-col>
        <b-col cols="6" sm="3">
          <div class="p-3 border border-dashed border-start-0 border-end-0">
            <h5 class="mb-1 text-success">
              <count-to :duration="1000" :startVal='0' :endVal="10589"></count-to>h
            </h5>
            <p class="text-muted mb-0">Working Hours</p>
          </div>
        </b-col>
      </b-row>
    </b-card-header>
    <b-card-body class="p-0 pb-2">
      <div>
        <apexchart class="apex-charts" height="374" dir="ltr" :series="series" :options="chartOptions"></apexchart>
      </div>
    </b-card-body>
  </b-card>
</template>