<script>
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
  setup() {
    return {
      series: [{
        name: "Pending",
        data: [80, 50, 30, 40, 100, 20],
      },
      {
        name: "Loss",
        data: [20, 30, 40, 80, 20, 80],
      },
      {
        name: "Won",
        data: [44, 76, 78, 13, 43, 10],
      },
      ],
      chartOptions: {
        chart: {
          height: 341,
          type: "radar",
          dropShadow: {
            enabled: true,
            blur: 1,
            left: 1,
            top: 1,
          },
          toolbar: {
            show: false,
          },
        },
        stroke: {
          width: 2,
        },
        fill: {
          opacity: 0.2,
        },
        legend: {
          show: true,
          fontWeight: 500,
          offsetX: 0,
          offsetY: -8,
          markers: {
            width: 8,
            height: 8,
            radius: 6,
          },
          itemMargin: {
            horizontal: 10,
            vertical: 0,
          },
        },
        markers: {
          size: 0,
        },
        colors: getChartColorsArray('["--vz-warning", "--vz-danger", "--vz-success"]'),
        xaxis: {
          categories: ["2016", "2017", "2018", "2019", "2020", "2021"],
        },
      },
    };
  },
};
</script>

<template>
  <b-card no-body class="card-height-100">
    <b-card-header class="align-items-center d-flex">
      <b-card-title class="mb-0 flex-grow-1">Deal Type</b-card-title>
      <div class="flex-shrink-0">
        <div class="dropdown card-header-dropdown">
          <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown" aria-haspopup="true"
            aria-expanded="false">
            <span class="fw-semibold text-uppercase fs-12">Sort by: </span><span class="text-muted">Monthly<i
                class="mdi mdi-chevron-down ms-1"></i></span>
          </b-link>
          <div class="dropdown-menu dropdown-menu-end">
            <b-link class="dropdown-item" href="#">Today</b-link>
            <b-link class="dropdown-item" href="#">Weekly</b-link>
            <b-link class="dropdown-item" href="#">Monthly</b-link>
            <b-link class="dropdown-item" href="#">Yearly</b-link>
          </div>
        </div>
      </div>
    </b-card-header>
    <b-card-body class="pb-0">
      <apexchart class="apex-charts" height="341" dir="ltr" :series="series" :options="chartOptions"></apexchart>
    </b-card-body>
  </b-card>
</template>