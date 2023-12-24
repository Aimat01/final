<template>
    <div :style="dividerStyle"></div>
  </template>
  
  <script>
  export default {
    props: {
      height: {
        type: String,
        default: '1px',
      },
      color: {
        type: String,
        default: '#ccc',
      },
    },
    computed: {
      dividerStyle() {
        return {
          borderTop: `solid ${this.height} ${this.color}`,
        };
      },
    },
  };
  </script>
  
  <style>
  /* No specific styles as it's all dynamic */
  </style>
  