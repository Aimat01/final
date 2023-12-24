<template>
    <div>
      <canvas ref="chartRef"></canvas>
    </div>
  </template>
  
  <script>
  export default {
    mounted() {
      this.renderChart();
    },
    methods: {
      renderChart() {
        const ctx = this.$refs.chartRef.getContext('2d');
        new window.Chart(ctx, {
          type: 'line',
          data: {
            labels: ['January', 'February', 'March', 'April', 'May'],
            datasets: [{
              label: 'Sample Data',
              borderColor: '#3498db',
              data: [10, 20, 15, 25, 30],
            }]
          },
          options: {}
        });
      }
    }
  }
  </script>
  