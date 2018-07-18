<template>
  <div>
    <div class="chart">
      <bar-chart
        :dataModel='byGender'
        propID='gender-bar-chart'
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
  data() {
    return {
      byGender: []
    };
  },
  mounted() {
    axios.get("http://localhost:3000/characters/gender").then(response => {
      this.byGender = response.data;
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
