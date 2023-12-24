<template>
    <div class="tooltip-container" @mouseover="showTooltip" @mouseout="hideTooltip">
      <slot></slot>
      <div v-if="isTooltipVisible" class="tooltip">
        {{ text }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      text: {
        type: String,
        default: "Tooltip text here"
      }
    },
    data() {
      return {
        isTooltipVisible: false
      };
    },
    methods: {
      showTooltip() {
        this.isTooltipVisible = true;
      },
      hideTooltip() {
        this.isTooltipVisible = false;
      }
    }
  };
  </script>
  
  <style scoped>
  .tooltip-container {
    position: relative;
    display: inline-block;
    cursor: pointer;
  }
  
  .tooltip {
    position: absolute;
    bottom: 100%;
    left: 50%;
    transform: translateX(-50%);
    background-color: #333;
    color: #fff;
    padding: 5px 10px;
    border-radius: 4px;
    opacity: 0;
    transition: opacity 0.3s;
    pointer-events: none; /* Ensures tooltip doesn't interfere with hover event */
  }
  
  .tooltip-container:hover .tooltip {
    opacity: 1;
  }
  </style>
  