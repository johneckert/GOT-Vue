<template>
  <div>
    <div class="chart">
      <bar-chart
        :dataModel='byName'
        propID='lastname-bar-chart'
        metric='Last Sale Price'
        title='Deaths By Gender'
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
      byName: []
    };
  },
  mounted() {
    axios.get("http://localhost:3000/characters/name").then(response => {
      this.byName = response.data;
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
