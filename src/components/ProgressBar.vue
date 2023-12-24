<template>
    <div class="container">
        <div class="progress-bar-container">
            <div class="progress-bar" :style="{ width: progress + '%' }"></div>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      value: {
        type: Number,
        default: 0,
        validator: value => value >= 0 && value <= 100
      }
    },
    computed: {
      progress() {
        return this.value;
      }
    }
  };
  </script>
  
  <style scoped>
    .container{
        display: flex;
        justify-content: center;
        padding-top: 40px;
    }
    .progress-bar-container {
    width: 50%;
    background-color: #e0e0e0;
    height: 20px;
    border-radius: 10px;
  }
  
  .progress-bar {
    height: 100%;
    background-color: #198568;
    border-radius: 8px;
    transition: width 0.3s ease-in-out;
  }
  </style>
  