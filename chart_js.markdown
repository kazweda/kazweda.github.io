---
layout: page
title: Chart.js
permalink: /chartjs/
---

<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.min.js"></script>
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById('myChart').getContext('2d');
new Chart(ctx, {
  type: "bar",
  data: {
    labels: ["January", "February", "March", "April"],
    datasets: [{
        label: "Bar Dataset",
        data: [10,20,30,40],
        borderColor: "rgb(255, 99, 132)",
        backgroundColor: "rgba(255, 99, 132, 0.2)"
      },{
        label: "Line Dataset",
        data: [50,45,40,35],
        type: "line",
        fill: false,
        borderColor: "rgb(54, 162, 235)"
    }]
  },
  options: {
    scales:{
      yAxes: [{
        ticks: {
          beginAtZero: true
        }
      }]
    }
  }
});
</script>