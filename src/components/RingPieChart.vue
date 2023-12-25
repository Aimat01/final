<template>
    <div>
      <canvas ref="pieCanvas" :width="canvasSize" :height="canvasSize"></canvas>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      size: {
        type: Number,
        default: 200
      },
      percentage1: {
        type: Number,
        required: true
      },
      percentage2: {
        type: Number,
        required: true
      },
      color1: {
        type: String,
        default: 'blue'
      },
      color2: {
        type: String,
        default: 'red'
      },
      centerText: {
        type: String,
        default: 'Center'
      }
    },
    computed: {
      canvasSize() {
        return this.size;
      }
    },
    mounted() {
      this.drawChart();
    },
    methods: {
      drawChart() {
        const canvas = this.$refs.pieCanvas;
        const ctx = canvas.getContext('2d');
        const centerX = canvas.width / 2;
        const centerY = canvas.height / 2;
  
        const radius = this.size / 2 - 5; // Adjusted for the border
        const innerRadius = radius * 0.8  ; // 90% of the main radius for the inner circle
  
        const startAngle1 = 0;
        const endAngle1 = (2 * Math.PI * this.percentage1) / 100;
  
        const startAngle2 = endAngle1;
        const endAngle2 = startAngle2 + (2 * Math.PI * this.percentage2) / 100;
  
        // Draw the outer circle (border)
        ctx.beginPath();
        ctx.arc(centerX, centerY, radius, 0, 2 * Math.PI);
        ctx.strokeStyle = '#9cb6ff'; // Border color
        ctx.lineWidth = 1; // Border width
        ctx.stroke();
  
        // Draw the first segment
        ctx.beginPath();
        ctx.moveTo(centerX, centerY);
        ctx.arc(centerX, centerY, radius, startAngle1, endAngle1);
        ctx.closePath();
        ctx.fillStyle = this.color1;
        ctx.fill();
  
        // Draw the second segment
        ctx.beginPath();
        ctx.moveTo(centerX, centerY);
        ctx.arc(centerX, centerY, radius, startAngle2, endAngle2);
        ctx.closePath();
        ctx.fillStyle = this.color2;
        ctx.fill();
  
        // Draw the inner circle
        ctx.beginPath();
        ctx.arc(centerX, centerY, innerRadius, 0, 2 * Math.PI);
        ctx.fillStyle = 'white'; // Inner circle color
        ctx.fill();

        ctx.fillStyle = 'blue';
        ctx.font = 'bold 17px sans-serif';
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillText(this.centerText, centerX, centerY);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Add any custom styles here */
  </style>
  