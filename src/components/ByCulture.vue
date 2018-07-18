<template>
  <div>
    <div class="chart">
      <bar-chart
        :dataModel='byCulture'
        propID='culture-bar-chart'
        metric='Last Sale Price'
        title='Deaths By Culture'
      ></bar-chart>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { D3BarChart } from "jscatalyst";

export default {
  data: function() {
    return {
      byCulture: []
    };
  },
  mounted() {
    axios.get("http://localhost:3000/characters/culture").then(response => {
      this.byCulture = response.data;
    });
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
