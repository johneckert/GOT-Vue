<template>
  <div>
    <div class="chart">
      <bar-chart
        :dataModel='barChartData'
        propID='lastname-bar-chart'
        metric='Last Sale Price'
        title='Deaths By Gender'
      ></bar-chart>
    </div>
  </div>
</template>

<script>
import { D3BarChart } from "jscatalyst";

export default {
  data: function() {
    return {
      barChartData: [
        { x: "A", y: 100 },
        { x: "B", y: 60 },
        { x: "C", y: 30 },
        { x: "D", y: 70 },
        { x: "E", y: 30 },
        { x: "F", y: 40 },
        { x: "G", y: 20 },
        { x: "H", y: 80 },
        { x: "I", y: 120 },
        { x: "J", y: 880 },
        { x: "K", y: 99 },
        { x: "L", y: 15 },
        { x: "M", y: 0 },
        { x: "N", y: 60 },
        { x: "O", y: 0 },
        { x: "P", y: 78 },
        { x: "Q", y: 112 },
        { x: "R", y: 11 },
        { x: "S", y: 62 },
        { x: "T", y: 6 },
        { x: "U", y: 77 },
        { x: "V", y: 44 },
        { x: "W", y: 65 },
        { x: "X", y: 30 },
        { x: "Y", y: 29 },
        { x: "Z", y: 60 }
      ]
    };
  },
  components: {
    "bar-chart": D3BarChart
  }
};
</script>

<style>
.chart {
  height: 400px;
  padding-top: 50px;
}
</style>
