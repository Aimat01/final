<template>
    <div class="containerFoot">
        <footer class="page-footer">
            <p>&copy; {{ currentYear }} Aimat's Website. All rights reserved.</p>
        </footer>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentYear: new Date().getFullYear()
      }
    }
  }
  </script>
  
  <style>
  .containerFoot{
    padding-top: 50px;
  }
  .page-footer {
    padding: 20px;
    text-align: center;
    background-color: #f5f5f5;
    border-top: 1px solid #ddd;
  }
  
  .page-footer p {
    margin: 0;
    color: #777;
    font-size: 14px;
  }
  </style>
  