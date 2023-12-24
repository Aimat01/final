<template>
    <div class="list-group">
      <div v-for="(item, index) in items" :key="index" class="list-group-item">
        {{ item }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      items: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  
  
  .list-group {
    width: 100%;
  }
  
  .list-group-item {
    padding: 10px;
    border-bottom: 1px solid #ddd;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }
  
  .list-group-item:hover {
    background-color: #f4f4f4;
  }
  </style>