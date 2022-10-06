<script setup>
import { onMounted } from "vue";

onMounted(() => {
  google.charts.load("current", { packages: ["geochart"] });

  google.charts.setOnLoadCallback(drawCountryChart);
  function drawCountryChart() {
    var data = new google.visualization.arrayToDataTable([
      ["State", "Select"],
      ["IN-AP", 0],
      ["IN-AR", 0],
      ["IN-AS", 0],
      ["IN-BR", 0],
      ["IN-CT", 0],
      ["IN-GA", 0],
      ["IN-GJ", 0],
      ["IN-HR", 0],
      ["IN-HP", 0],
      ["IN-JH", 0],
      ["IN-KA", 0],
      ["IN-KL", 0],
      ["IN-MP", 0],
      ["IN-MH", 0],
      ["IN-MN", 0],
      ["IN-ML", 0],
      ["IN-MZ", 0],
      ["IN-NL", 0],
      ["IN-OR", 0],
      ["IN-PB", 0],
      ["IN-RJ", 0],
      ["IN-SK", 0],
      ["IN-TN", 0],
      ["IN-TG", 0],
      ["IN-TR", 0],
      ["IN-UT", 0],
      ["IN-UP", 0],
      ["IN-WB", 0],
      ["IN-AN", 0],
      ["IN-CH", 0],
      ["IN-DH", 0],
      ["IN-DL", 0],
      ["IN-JK", 0],
      ["IN-LA", 0],
      ["IN-LD", 0],
      ["IN-PY", 0],
    ]);

    var options = {
      region: "IN",
      magnifyingGlass: {
        enable: true,
      },
      displayMode: "regions",
      resolution: "provinces",
      title: "How Much Pizza I Ate Last Night",
      width: 920,
      height: 780,
    };

    var chart = new google.visualization.GeoChart(
      document.getElementById("chart_div")
    );
    chart.draw(data, options);
  }
});
</script>

<template>
  <div id="chart_div"></div>
</template>
