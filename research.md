---
layout: default
title: Research
description:
---

# Research and Development
Geoinformatics Laboratory, IIT Kanpur has been contributing to the national development and international scientific community by carrying out original research and development in various areas. Various consultancy and sponsored research projects undertaken by the laboratory are listed here.<br>
* * *
## Sponsored Research Projects
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Project Summary</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    canvas {
      max-width: 400px;
      margin: 20px;
    }
  </style>
</head>
<body>
  <h1>Project Summary</h1>

  <h2>Total Sponsored Projects Summary</h2>
  <canvas id="sponsoredProjectsChart"></canvas>
  <canvas id="sponsoredCostChart"></canvas>
  <p>Major Funding Agencies: MHRD, DST, DRDO</p>

  <h2>Total Consultancy Projects Summary</h2>
  <canvas id="consultancyProjectsChart"></canvas>
  <canvas id="consultancyCostChart"></canvas>
  <p>Major Funding Bodies: NGRI-CSIR, SMVDSB/THDC, THDC</p>

  <h2>Areas of Projects</h2>
  <ul>
    <li>LiDAR</li>
    <li>Remote Sensing</li>
    <li>Earthquake Modeling</li>
    <!-- Add more areas as needed -->
  </ul>

  <script>
    // Sponsored Projects Data
    var sponsoredProjectsData = {
      labels: ['MHRD', 'DST', 'DRDO'],
      datasets: [{
        label: 'Number of Projects',
        data: [4, 4, 4],
        backgroundColor: ['#ff6384', '#36a2eb', '#ffce56']
      }]
    };

    var sponsoredCostData = {
      labels: ['MHRD', 'DST', 'DRDO'],
      datasets: [{
        label: 'Total Cost (in millions)',
        data: [40, 30, 25],
        backgroundColor: ['#ff6384', '#36a2eb', '#ffce56']
      }]
    };

    // Consultancy Projects Data
    var consultancyProjectsData = {
      labels: ['NGRI-CSIR', 'SMVDSB/THDC', 'THDC'],
      datasets: [{
        label: 'Number of Projects',
        data: [1, 1, 2],
        backgroundColor: ['#ff6384', '#36a2eb', '#ffce56']
      }]
    };

    var consultancyCostData = {
      labels: ['NGRI-CSIR', 'SMVDSB/THDC', 'THDC'],
      datasets: [{
        label: 'Total Cost (in millions)',
        data: [5, 3, 10],
        backgroundColor: ['#ff6384', '#36a2eb', '#ffce56']
      }]
    };

    // Render Charts
    var sponsoredProjectsChart = new Chart(document.getElementById('sponsoredProjectsChart'), {
      type: 'pie',
      data: sponsoredProjectsData
    });

    var sponsoredCostChart = new Chart(document.getElementById('sponsoredCostChart'), {
      type: 'bar',
      data: sponsoredCostData
    });

    var consultancyProjectsChart = new Chart(document.getElementById('consultancyProjectsChart'), {
      type: 'pie',
      data: consultancyProjectsData
    });

    var consultancyCostChart = new Chart(document.getElementById('consultancyCostChart'), {
      type: 'bar',
      data: consultancyCostData
    });
  </script>
</body>
</html>