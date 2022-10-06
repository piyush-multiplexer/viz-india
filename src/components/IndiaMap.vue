<script setup>
import { onMounted } from "vue";

onMounted(() => {
  google.charts.load("current", { packages: ["geochart"] });

  google.charts.setOnLoadCallback(drawCountryChart);
  function drawCountryChart() {
    var data = new google.visualization.arrayToDataTable([
      ["State", "Text label", "Select"],
      ["IN-AP", "Andhra Pradesh", 0],
      ["IN-AR", "Arunachal Pradesh", 0],
      ["IN-AS", "Assam", 0],
      ["IN-BR", "Bihar", 0],
      ["IN-CT", "Chhattisgarh", 0],
      ["IN-GA", "Goa", 0],
      ["IN-GJ", "Gujarat", 0],
      ["IN-HR", "Haryana", 0],
      ["IN-HP", "Himachal Pradesh", 0],
      ["IN-JH", "Jharkhand", 0],
      ["IN-KA", "Karnataka", 0],
      ["IN-KL", "Kerala", 0],
      ["IN-MP", "Madhya Pradesh", 0],
      ["IN-MH", "Maharashtra", 0],
      ["IN-MN", "Manipur", 0],
      ["IN-ML", "Meghalaya", 0],
      ["IN-MZ", "Mizoram", 0],
      ["IN-NL", "Nagaland", 0],
      ["IN-OR", "Odisha", 0],
      ["IN-PB", "Punjab", 0],
      ["IN-RJ", "Rajasthan", 0],
      ["IN-SK", "Sikkim", 0],
      ["IN-TN", "Tamil Nadu", 0],
      ["IN-TG", "Telangana", 0],
      ["IN-TR", "Tripura", 0],
      ["IN-UT", "Uttarakhand", 0],
      ["IN-UP", "Uttar Pradesh", 0],
      ["IN-WB", "West Bengal", 0],
      ["IN-AN", "Andaman and Nicobar Islands", 0],
      ["IN-CH", "Chandigarh", 0],
      ["IN-DH", "Dadra and Nagar Haveli and Daman and Diu", 0],
      ["IN-DL", "Delhi", 0],
      ["IN-JK", "Jammu and Kashmir", 0],
      ["IN-LA", "Ladakh", 0],
      ["IN-LD", "Lakshadweep", 0],
      ["IN-PY", "Puducherry", 0],
    ]);

    var options = {
      domain: "IN", // show disputed regions e.g kashmir from IN point-view
      region: "IN",
      displayMode: "region",
      resolution: "provinces",
      enableRegionInteractivity: true,
      magnifyingGlass: {
        enable: true,
      },
      tooltip: { textStyle: { color: "#CF56F0" }, showColorCode: true },
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
