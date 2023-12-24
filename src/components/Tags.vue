<template>
    <div class="container">
    <div class="tags">
      <span v-for="tag in tags" :key="tag" class="tag">{{ tag }}</span>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      tags: {
        type: Array,
        required: true
      }
    }
  }
  </script>
  