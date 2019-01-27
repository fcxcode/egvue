<template>
  <div>
    <h1>{{ title }}</h1>
    <div style="width:65%; margin: auto;">
      <canvas id="activities-charts"></canvas>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js";
import activitiesChartsData from "../chart-data.js";

export default {
  name: "ActivitiesCharts",
  props: {
    title: String
  },
  data() {
    return {
      activitiesChartsData: activitiesChartsData
    };
  },
  mounted() {
    this.createChart("activities-charts", this.activitiesChartsData);
  },
  methods: {
    createChart(chartId, chartData) {
      const ctx = document.getElementById(chartId);
      new Chart(ctx, {
        type: chartData.type,
        data: chartData.data,
        options: chartData.options
      });
    }
  }
};
</script>