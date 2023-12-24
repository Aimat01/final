<template>
    <div class="tabs">
      <div class="tab-header">
        <div
          v-for="tab in tabs"
          :key="tab.id"
          @click="selectedTab = tab.id"
          :class="{ 'active': selectedTab === tab.id }"
        >
          {{ tab.title }}
        </div>
      </div>
      <div class="tab-content">
        <slot :name="`tab-${selectedTab}`"></slot>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedTab: 1, // Default to the first tab
        tabs: [
          { id: 1, title: 'Tab 1' },
          { id: 2, title: 'Tab 2' },
          { id: 3, title: 'Tab 3' },
          // ... add more tabs as needed
        ],
      };
    },
  };
  </script>
  
  <style>
  .tabs {
    /* styling for the tabs component */
  }
  .tab-header {
    display: flex;
    border-bottom: 1px solid #ccc;
  }
  .tab-header div {
    padding: 10px 20px;
    cursor: pointer;
    border-right: 1px solid #ccc;
  }
  .tab-header div:last-child {
    border-right: none;
  }
  .tab-header .active {
    background-color: #f4f4f4;
    color: black;
  }
  .tab-content {
    padding: 20px;
  }
  </style>
  