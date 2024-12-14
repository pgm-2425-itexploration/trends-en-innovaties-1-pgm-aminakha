<script>
      import { onMount } from 'svelte';
  import { Chart, registerables } from 'chart.js';

  Chart.register(...registerables);

  let chart;

  const data = {
  labels: ['2019', '2020', '2021', '2022', '2023', '2024'],
  datasets: [
    {
      label: 'Svelte',
      data: [2, 4, 10, 20, 35, 50], // Svelte has been growing steadily, but still smaller
      borderColor: 'rgba(255, 99, 132, 1)',
      backgroundColor: 'rgba(255, 99, 132, 0.3)',
      pointBackgroundColor: 'rgba(255, 99, 132, 1)',
      pointHoverRadius: 8,
      borderWidth: 3,
      tension: 0.4,
      fill: true,
    },
    {
      label: 'React',
      data: [70, 75, 80, 85, 90, 92], // React has a strong, consistent rise in popularity
      borderColor: 'rgba(54, 162, 235, 1)',
      backgroundColor: 'rgba(54, 162, 235, 0.3)',
      pointBackgroundColor: 'rgba(54, 162, 235, 1)',
      pointHoverRadius: 8,
      borderWidth: 3,
      tension: 0.4,
      fill: true,
    },
    {
      label: 'Vue',
      data: [45, 50, 55, 60, 65, 70], // Vue steadily growing, but not as fast as React
      borderColor: 'rgba(75, 192, 192, 1)',
      backgroundColor: 'rgba(75, 192, 192, 0.3)',
      pointBackgroundColor: 'rgba(75, 192, 192, 1)',
      pointHoverRadius: 8,
      borderWidth: 3,
      tension: 0.4,
      fill: true,
    },
    {
      label: 'Angular',
      data: [60, 62, 63, 64, 65, 67], // Angular has slower growth and is more stable
      borderColor: 'rgba(255, 206, 86, 1)',
      backgroundColor: 'rgba(255, 206, 86, 0.3)',
      pointBackgroundColor: 'rgba(255, 206, 86, 1)',
      pointHoverRadius: 8,
      borderWidth: 3,
      tension: 0.4,
      fill: true,
    },
  ],
};

  onMount(() => {
    const ctx = document.getElementById('usageChart').getContext('2d');
    chart = new Chart(ctx, {
      type: 'line',
      data,
      options: {
        responsive: true,
        plugins: {
          legend: {
            display: true,
            labels: {
              color: '#333',
              font: {
                size: 14,
                family: 'Arial, sans-serif',
              },
            },
          },
          tooltip: {
            enabled: true,
            backgroundColor: 'rgba(0, 0, 0, 0.7)',
            titleFont: {
              size: 16,
            },
            bodyFont: {
              size: 14,
            },
            bodyColor: '#fff',
            padding: 10,
            displayColors: false,
          },
        },
        scales: {
          x: {
            grid: {
              color: 'rgba(200, 200, 200, 0.3)',
            },
            ticks: {
              color: '#333',
              font: {
                size: 14,
                family: 'Arial, sans-serif',
              },
            },
          },
          y: {
            grid: {
              color: 'rgba(200, 200, 200, 0.3)',
            },
            ticks: {
              color: '#333',
              font: {
                size: 14,
                family: 'Arial, sans-serif',
              },
            },
          },
        },
        animation: {
          duration: 2000,
          easing: 'easeInOutCubic',
        },
      },
    });
  });
</script>
<canvas id="usageChart" class="usage-chart" width="400" height="202"></canvas>

<style>
       canvas {
    display: block;
    max-width: 600px;
    margin: 0 auto;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    margin-bottom: 1rem;
    border: solid 2px #b0b0b0;
  }

  .usage-chart {
    padding: 1rem;
    background: linear-gradient(120deg, #f7f7f7, #ffffff);
    border-radius: 15px;
  }
</style>