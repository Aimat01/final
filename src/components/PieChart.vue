<template>
    <div class="chart-container">
      <canvas ref="pieCanvas"></canvas>
      <Circle class="Google" content="20% Google"></Circle>
      <Circle class="Website" content="50% Website"></Circle>
      <Circle class="Others" content="30% Others"></Circle>
    </div>
  </template>
  
  <script>
import Circle from './Circle.vue';

  export default {
    mounted() {
        this.drawChart();
    },
    methods: {
        drawChart() {
            const canvas = this.$refs.pieCanvas;
            const ctx = canvas.getContext('2d');
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const radius = Math.min(centerX, centerY);
            const websitePercentage = 50;
            const googlePercentage = 30;
            const otherPercentage = 20;
            // Function to draw a ring slice
            const drawRingSlice = (startAngle, endAngle, color) => {
                ctx.fillStyle = color;
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.arc(centerX, centerY, radius, startAngle, endAngle);
                ctx.lineTo(centerX, centerY);
                ctx.fill();
            };
            // Draw the ring slices
            const websiteEndAngle = (2 * Math.PI * websitePercentage) / 100;
            drawRingSlice(0, websiteEndAngle, '#0d72d6');
            const googleStartAngle = websiteEndAngle;
            const googleEndAngle = googleStartAngle + (2 * Math.PI * googlePercentage) / 100;
            drawRingSlice(googleStartAngle, googleEndAngle, 'white');
            const otherStartAngle = googleEndAngle;
            const otherEndAngle = otherStartAngle + (2 * Math.PI * otherPercentage) / 100;
            drawRingSlice(otherStartAngle, otherEndAngle, '#ebc623');
            // Draw the inner circle to create the ring effect
            ctx.fillStyle = 'white';
            ctx.beginPath();
            ctx.arc(centerX, centerY, radius * 0.5, 0, 2 * Math.PI);
            ctx.fill();
        },
    },
    components: { Circle }
};
  </script>
  
  <style scoped>
  /* Add any custom styles here */
  .chart-container {
  position: relative;
}

.Website {
  position: absolute;
  top: 73%;
  left: 51%;
  transform: translate(-50%, -50%);
}

.Google {
  position: absolute;
  top: 15%;
  left: 71%;
  transform: translate(-50%, -50%);
}

.Others {
  position: absolute;
  top: 10%;
  left: 37%;
  transform: translate(-50%, -50%);
}
  </style>
  