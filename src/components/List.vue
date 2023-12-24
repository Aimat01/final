<template>
    <ul class="custom-list">
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
  </template>
  
  <script>
  export default {
    props: {
      items: {
        type: Array,
        required: true,
        validator: (array) => array.every((item) => typeof item === 'string')
      }
    }
  }
  </script>
  
  <style scoped>
  .custom-list {
    list-style-type: none;
    padding: 0;
  }
  
  .custom-list li {
    padding: 8px 0;
    border-bottom: 1px solid #e0e0e0;
  }
  
  .custom-list li:last-child {
    border-bottom: none;
  }
  </style>
  