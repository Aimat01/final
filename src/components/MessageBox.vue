<template>
    <div class="container">
        <div class="message-box" :class="type">
            {{ message }}
        </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      message: {
        type: String,
        required: true
      },
      type: {
        type: String,
        default: 'info'  // Other options: 'error', 'warning', 'success'
      }
    }
  }
  </script>
  
  <style>
  .message-box {
    padding: 10px 15px;
    border-radius: 4px;
    margin-bottom: 10px;
  }
  
  .info {
    background-color: #e0f7fa;
    color: #00acc1;
  }
  
  .error {
    background-color: #ffcdd2;
    color: #f44336;
  }
  
  .warning {
    background-color: #ffe0b2;
    color: #ff9800;
  }
  
  .success {
    background-color: #d0f8ce;
    color: #4caf50;
  }
  </style>
  