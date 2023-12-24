<template>
    <div class="grid-container">
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* Example: 3 columns */
    gap: 16px; /* Space between grid items */
  }
  </style>
  