---
layout: default
title: Research
description:
---

# Research and Development

Geoinformatics Laboratory, IIT Kanpur has been contributing to the national development and international scientific community by carrying out original research and development in various areas. Various consultancy and sponsored research projects undertaken by the laboratory are listed here.

* * *


<html lang="{{ site.lang | default: "en-US" }}">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Project Summary</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f5f5f5;
      color: #333;
      margin: 0;
      padding: 20px;
    }

    .container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }

    .chart-container {
      background-color: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      flex: 0 1 45%; /* Adjust the width as needed */
    }

    h1, h2, h3 {
      margin-top: 0;
    }

    canvas {
      max-width: 100%; /* Make sure canvas doesn't exceed its container */
      margin: 0 auto; /* Center the canvas horizontally */
      display: block;
      border-radius: 5px;
      box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
    }

    ul {
      padding-left: 20px;
    }

    .y-axis-label {
      position: absolute;
      transform: rotate(-90deg);
      left: -30px;
      top: 50%;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="chart-container">
      <h2>Total Sponsored Projects Summary</h2>
      <div class="chart-container">
        <canvas id="sponsoredProjectsChart"></canvas>
      </div>
      <div class="chart-container">
        <canvas id="sponsoredCostChart"></canvas>
      </div>
      <p><strong>Major Funding Agencies:</strong> MHRD, DST, DRDO</p>
    </div>

    <div class="chart-container">
      <h2>Total Consultancy Projects Summary</h2>
      <div class="chart-container">
        <canvas id="consultancyProjectsChart"></canvas>
      </div>
      <div class="chart-container">
        <canvas id="consultancyCostChart"></canvas>
      </div>
      <p><strong>Major Funding Bodies:</strong> NGRI-CSIR, SMVDSB/THDC, THDC</p>
    </div>
  </div>

  <script>
    // Sponsored Projects Data
    var sponsoredProjectsData = {
      labels: ['MHRD', 'DST', 'DRDO'],
      datasets: [{
        label: 'Number of Projects',
        data: [4, 4, 4],
        backgroundColor: ['#ff9999', '#99ff99', '#9999ff'] // Different colors for each dataset
      }]
    };

    var sponsoredCostData = {
      labels: ['MHRD', 'DST', 'DRDO'],
      datasets: [{
        label: 'Total Cost (in millions ₹)', // Added ₹ for Indian Rupees
        data: [40, 30, 25],
        backgroundColor: ['#ff9999', '#99ff99', '#9999ff'] // Different colors for each dataset
      }]
    };

    // Consultancy Projects Data
    var consultancyProjectsData = {
      labels: ['NGRI-CSIR', 'SMVDSB/THDC', 'THDC'],
      datasets: [{
        label: 'Number of Projects',
        data: [1, 1, 2],
        backgroundColor: ['#ffcc99', '#ccff99', '#99ffcc'] // Different colors for each dataset
      }]
    };

    var consultancyCostData = {
      labels: ['NGRI-CSIR', 'SMVDSB/THDC', 'THDC'],
      datasets: [{
        label: 'Total Cost (in millions ₹)', // Added ₹ for Indian Rupees
        data: [5, 3, 10],
        backgroundColor: ['#ffcc99', '#ccff99', '#99ffcc'] // Different colors for each dataset
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

    // Add Y-axis labels
    var sponsoredCostChartInstance = new Chart(document.getElementById('sponsoredCostChart'), {
      type: 'bar',
      data: sponsoredCostData,
      options: {
        scales: {
          yAxes: [{
            ticks: {
              callback: function(value, index, values) {
                return value + ' ₹'; // Add ₹ for Indian Rupees
              }
            }
          }]
        }
      }
    });

    var consultancyCostChartInstance = new Chart(document.getElementById('consultancyCostChart'), {
      type: 'bar',
      data: consultancyCostData,
      options: {
        scales: {
          yAxes: [{
            ticks: {
              callback: function(value, index, values) {
                return value + ' ₹'; // Add ₹ for Indian Rupees
              }
            }
          }]
        }
      }
    });
  </script>
</body>
</html>
