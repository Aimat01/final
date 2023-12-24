<template>
    <div class="container">
        <input type="date" :value="selectedDate" @input="updateDate" />
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedDate: '',
      };
    },
    methods: {
      updateDate(event) {
        this.selectedDate = event.target.value;
        this.$emit('input', this.selectedDate);
      },
    },
  };
  </script>
  
  <style>
  </style>
  