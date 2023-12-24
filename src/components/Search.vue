<template>
    <div class="search-bar">
      <input type="text" v-model="query" @input="search" placeholder="Search Dashboard">
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        query: ''
      }
    },
    methods: {
      search() {
      }
    }
  }
  </script>
  
  <style>
  .search-bar {
    display: flex;
    align-items: center;
    padding: 10px;
    border-radius: 4px;
  }
  
  .search-bar input {
    flex: 1;
    padding: 8px;
    margin-right: 10px;
    border: none;
    outline: none;
    border-radius: 4px;
  }
  </style>
  