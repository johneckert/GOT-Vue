<template>
  <div>
    <div class="chart">
      <bar-chart
        :dataModel='barChartData'
        propID='gender-bar-chart'
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
      barChartData: [{ x: "Male", y: 60 }, { x: "Female", y: 30 }]
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
