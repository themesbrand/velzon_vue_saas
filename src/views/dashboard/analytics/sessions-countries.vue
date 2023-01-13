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
        data: [1010, 1640, 490, 1255, 1050, 689, 800, 420, 1085, 589],
        name: "Sessions",
      },],
      chartOptions: {
        chart: {
          type: "bar",
          height: 436,
          toolbar: {
            show: false,
          },
        },
        plotOptions: {
          bar: {
            borderRadius: 4,
            horizontal: true,
            distributed: true,
            dataLabels: {
              position: "top",
            },
          },
        },
        colors: getChartColorsArray(
          '["--vz-info", "--vz-info", "--vz-info", "--vz-info", "--vz-danger", "--vz-info", "--vz-info", "--vz-info", "--vz-info", "--vz-info"]'
        ),
        dataLabels: {
          enabled: true,
          offsetX: 32,
          style: {
            fontSize: "12px",
            fontWeight: 400,
            colors: ["#adb5bd"],
          },
        },

        legend: {
          show: false,
        },
        grid: {
          show: false,
        },
        xaxis: {
          categories: [
            "India",
            "United States",
            "China",
            "Indonesia",
            "Russia",
            "Bangladesh",
            "Canada",
            "Brazil",
            "Vietnam",
            "UK",
          ],
        },
      },
    };
  },
};
</script>

<template>
  <b-card no-body class="card-height-100">
    <b-card-header class="align-items-center d-flex">
      <b-card-title class="mb-0 flex-grow-1">Sessions by Countries</b-card-title>
      <div class="hstack gap-1">
        <b-button type="button" variant="soft-secondary" size="sm">ALL</b-button>
        <b-button type="button" variant="soft-primary" size="sm">1M</b-button>
        <b-button type="button" variant="soft-secondary" size="sm">6M</b-button>
      </div>
    </b-card-header>
    <b-card-body class="p-0">
      <div>
        <apexchart class="apex-charts" dir="ltr" height="436" :series="series" :options="chartOptions"></apexchart>
      </div>
    </b-card-body>
  </b-card>
</template>