<template>
  <div>
    <div class="chart">
      <bar-chart
        :dataModel='barChartData'
        propID='culture-bar-chart'
        metric='Last Sale Price'
        title='Deaths By Culture'
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
        { x: "Targaryen", y: 0.5 },
        { x: "Northmen", y: 0.7 },
        { x: "Ironborn", y: 0.3 }
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
